// Função para adicionar uma nova tarefa à lista do campo
function addTask() {
    const input = document.getElementById('taskInput');
    const taskText = input.value.trim();

    // Impede adicionar tarefas em branco
    if (taskText === "") {
        alert("Por favor, digite uma tarefa válida!");
        return;
    }

    const ul = document.getElementById('taskList');

    // Cria o item da lista (li)
    const li = document.createElement('li');

    // Cria o texto da tarefa
    const textSpan = document.createElement('span');
    textSpan.innerText = taskText;
    li.appendChild(textSpan);

    // Garante estrutura para os botões de ação
    const btnContainer = document.createElement('div');
    btnContainer.className = "task-buttons";

    // Botão Concluir
    const doneBtn = document.createElement('button');
    doneBtn.className = "done-btn";
    doneBtn.innerText = "✓ Feito";
    doneBtn.onclick = function() {
        li.classList.toggle('completed');
    };

    // Botão Excluir
    const deleteBtn = document.createElement('button');
    deleteBtn.className = "delete-btn";
    deleteBtn.innerText = "🗑️ Apagar";
    deleteBtn.onclick = function() {
        ul.removeChild(li);
    };

    // Monta o item completo e adiciona na tela
    btnContainer.appendChild(doneBtn);
    btnContainer.appendChild(deleteBtn);
    li.appendChild(btnContainer);
    ul.appendChild(li);

    // Limpa o campo de entrada para a próxima tarefa
    input.value = "";
}

// Permite adicionar a tarefa pressionando a tecla "Enter"
document.getElementById('taskInput').addEventListener('keypress', function(e) {
    if (e.key === 'Enter') {
        addTask();
    }
});
