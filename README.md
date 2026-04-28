function addOthers() {
    const name = document.getElementById('others-name').value;
    const url = document.getElementById('others-url').value;
    if(!name || !url) return alert("入力してください");

    // 'others' というカテゴリを付けて保存用配列に追加
    const newItem = { name: name, url: url, category: 'others' };
    myUrls.push(newItem);
    localStorage.setItem('myUrls', JSON.stringify(myUrls));
    
    renderOthers(); // 表示更新
    alert("追加しました。同期ボタンで保存してください。");
}
