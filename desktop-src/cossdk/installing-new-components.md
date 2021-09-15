---
description: Para agregar componentes a la carpeta Componentes de una aplicación COM+, puede usar el Asistente para instalación de componentes COM+ o arrastrar archivos .dll que contengan los componentes desde el Explorador de Windows y colocarlos en la aplicación.
ms.assetid: 3cb0c24d-cd52-42ac-8b07-d8774698b90c
title: Instalación de nuevos componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434bdb59c0a0e9c786bb3460a0cb1cbb6a1f50dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359034"
---
# <a name="installing-new-components"></a>Instalación de nuevos componentes

Para agregar componentes  a la carpeta Componentes de una aplicación COM+, puede usar el Asistente para instalación de componentes COM+ o arrastrar archivos .dll que contengan los componentes desde el Explorador de Windows y colocarlos en la aplicación.

Si usa el Asistente para instalación de componentes COM+, puede instalar un nuevo componente, que registra el componente en el equipo, o importar componentes que ya se han registrado. Los componentes se pueden agregar a aplicaciones vacías o a aplicaciones existentes.

**Para agregar un componente a una aplicación COM+**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, seleccione el equipo que hospeda la aplicación COM+.

2.  Abra la **carpeta Aplicaciones COM+** para ese equipo y seleccione la aplicación en la que desea instalar los componentes.

3.  Abra la carpeta de la aplicación y seleccione **Componentes**.

4.  En el **menú Acción,** seleccione **Nuevo y,** a continuación, haga clic en **Componente**. También puede hacer clic con el botón derecho en la **carpeta Componentes,** seleccionar **Nuevo** y, a continuación, hacer clic en **Componente**.

5.  En la **página principal** del Asistente para instalación de aplicaciones COM+, haga clic en Siguiente y, **a** continuación, en el cuadro de diálogo Importar o instalar un componente , haga clic en Instalar **nuevos componentes** .

6.  En el **cuadro de diálogo Instalar** nuevos componentes , haga clic **en** Agregar para buscar el componente que desea agregar.

7.  En el **cuadro de diálogo Seleccionar archivos** para instalar, escriba el nombre de archivo del componente que se va a instalar o seleccione un nombre de archivo en la lista mostrada. Haga clic en **Abrir**.

    Después de agregar los archivos, el **cuadro de diálogo** Instalar nuevos componentes muestra los archivos que ha agregado y sus componentes asociados. Si selecciona la casilla **Detalles,** verá más información sobre el contenido del archivo y los componentes que se encontraron.

    > [!Note]  
    > Los componentes COM no configurados deben tener una biblioteca de tipos. Si COM+ no encuentra la biblioteca de tipos del componente, el componente no aparecerá en la lista. También puede quitar un archivo de la lista Archivos para **instalar** si lo selecciona y hace clic en **Quitar.**

     

8.  Haga **clic en Siguiente** y, a continuación, haga clic **en** Finalizar para instalar el componente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Copiar componentes](copying-components.md)
</dt> <dt>

[Creación de una nueva aplicación COM+](creating-a-new-com--application.md)
</dt> <dt>

[Eliminación de una aplicación COM+](deleting-a-com--application.md)
</dt> <dt>

[Importar componentes](importing-components.md)
</dt> <dt>

[Mover componentes](moving-components.md)
</dt> <dt>

[Quitar un componente de una aplicación COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



