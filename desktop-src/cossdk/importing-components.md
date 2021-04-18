---
description: Puede usar la herramienta administrativa Servicios de componentes para importar en componentes específicos de aplicaciones que ya se han registrado en el equipo como componentes COM en el registro de Windows.
ms.assetid: 5310e08a-5146-41f8-ae65-8467b921abd4
title: Importar componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b67d944e9b8880b3edd0583569155fffecb23b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496030"
---
# <a name="importing-components"></a>Importar componentes

Puede usar la herramienta administrativa Servicios de componentes para importar en componentes específicos de aplicaciones que ya se han registrado en el equipo como componentes COM en el registro de Windows. Al importar un componente, no se instala la interfaz o la información de método necesaria para establecer las propiedades de la interfaz o para configurar el acceso al componente desde un cliente remoto. Por lo tanto, si es posible, debe instalar en lugar de importar componentes sin configurar.

> [!Note]  
> Al importar un componente en una aplicación COM+, COM+ no rellena la información de interfaz y de método para el componente. Durante la exportación de un proxy de aplicación, COM+ no proporcionará información de serialización (bibliotecas de tipos o proxy/código auxiliar) para algunas o todas las interfaces. Se producirá un error en la exportación de proxies de aplicación que contienen componentes importados o se producirá una advertencia.

 

**Para importar un componente en una aplicación COM+**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, seleccione el equipo que hospeda la aplicación COM+.

2.  Abra la carpeta **aplicaciones com+** para ese equipo y seleccione la aplicación en la que desea instalar el componente.

3.  Abra la carpeta de la aplicación y seleccione **componentes**.

4.  En el menú **acción** , seleccione **nuevo** y, a continuación, haga clic en **componente**. También puede hacer clic con el botón secundario en la carpeta **componentes** , seleccionar **nuevo** y, a continuación, hacer clic en **componente**.

5.  En la página **principal** del Asistente para instalación de aplicaciones com+, haga clic en **siguiente** y, en el cuadro de diálogo **importar o instalar un componente** , haga clic en **importar componentes que ya están registrados**.

6.  En el cuadro de diálogo **elegir los componentes que se van a importar** , active la casilla **detalles** para ver información completa sobre los componentes que ya están registrados. Seleccione los componentes que desea importar en la lista que aparece y haga clic en **siguiente**.

7.  Haga clic en **Finalizar**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Copiar componentes](copying-components.md)
</dt> <dt>

[Crear una nueva aplicación COM+](creating-a-new-com--application.md)
</dt> <dt>

[Eliminar una aplicación COM+](deleting-a-com--application.md)
</dt> <dt>

[Instalación de nuevos componentes](installing-new-components.md)
</dt> <dt>

[Mover componentes](moving-components.md)
</dt> <dt>

[Quitar un componente de una aplicación COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



