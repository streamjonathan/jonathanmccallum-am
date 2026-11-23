---
title: "አንድ አርቲስት ጠቁም"
slug: suggest-an-artist
---

ኢየሱስን የሚከተሉ ሙዚቀኞችንና አርቲስቶችን መስማት በጣም እወዳለሁ። ስለ እነሱ ልጽፍ፣ ቃለ መጠይቅ ልጠይቅ ወይም ምላሽ ቪዲዮ ልሥራ የምትፈልገውን ሰው ታውቃለህ? እዚህ ንገረኝ።

አንድ ስምና አንድ አገናኝ በቂ ነው — ለምን እርሱ እንደሆነም በጥቂት ቃላት። የሚመጣውን ሁሉ እያነብኩ ነው። በጣም እናመሰግናለሁ።

የምታውቀው ሰው አለ? ፎቶውን ንካ፣ ቅጹ በራሱ ይሞላል — ከዚያ ለምን እርሱ እንደሆነ በጥቂት ቃላት ጨምር እና ላክ።

<div class="suggest-carousel" role="list" aria-label="ሊጠቁሙ የሚችሏቸው ሙዚቀኞችና አርቲስቶች">
{% for artist in suggest_carousel %}
  <button type="button" class="suggest-pick" role="listitem" data-artist="{{ artist.name }}" data-link="{{ artist.profile }}" title="{{ artist.name }}ን ጠቁም">
    <img src="{{ artist.img }}" alt="{{ artist.name }}" loading="lazy" width="150" height="150">
    <span class="suggest-pick__name">{{ artist.name }}</span>
    <span class="suggest-pick__note">{{ artist.note }}</span>
  </button>
{% endfor %}
</div>

<p class="suggest-carousel__more">ወይም ከዚህ በታች አዲስ ሰው ጠቁም — ልሰማው ይገባኛል የምትለውን ማንኛውንም ሰው።</p>

ይህ ድረ-ገጽ ከ18 ዓመት በታች ላሉት አይደለም።

<form id="suggest-form" class="suggest-form">
  <label for="suggest-artist">የአርቲስቱ ስም</label>
  <input id="suggest-artist" name="artist" type="text" maxlength="200" placeholder="ማንን ልመልከት?" required>

  <label for="suggest-link">የማህበራዊ ሚዲያ መገለጫ አገናኝ</label>
  <input id="suggest-link" name="link" type="url" maxlength="500" placeholder="https://www.instagram.com/…" required>

  <fieldset class="suggest-kinds">
    <legend>ከእነሱ ጋር ምን ላድርግ?</legend>
    <label><input type="checkbox" name="kind" value="write"> ስለ እነሱ ጻፍ</label>
    <label><input type="checkbox" name="kind" value="interview"> ቃለ መጠይቅ አድርግ</label>
    <label><input type="checkbox" name="kind" value="reaction"> ስለ እነሱ ምላሽ ቪዲዮ ሥራ</label>
  </fieldset>

  <label for="suggest-why">ለምን እርሱ?</label>
  <textarea id="suggest-why" name="why" rows="3" maxlength="500" placeholder="ጥቂት ቃላት በቂ ናቸው…"></textarea>

  <label for="suggest-name">ስምህ <span class="optional">(አማራጭ)</span></label>
  <input id="suggest-name" name="fromName" type="text" maxlength="100" placeholder="አመሰግንህ ዘንድ">

  <label for="suggest-from-link">የማህበራዊ ሚዲያ መገለጫ አገናኝህ <span class="optional">(አማራጭ)</span></label>
  <input id="suggest-from-link" name="fromLink" type="url" maxlength="500" placeholder="https://www.instagram.com/…">

  <button id="suggest-button" type="button">ጠቁሚውን ላክ</button>

  <p id="suggest-result" aria-live="polite"></p>
</form>
