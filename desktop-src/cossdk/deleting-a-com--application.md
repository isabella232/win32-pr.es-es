---
description: A medida que las aplicaciones existentes se hacen obsoletas o ya no se usan, puede que tenga que quitarlas.
ms.assetid: 5cce94c9-8eff-40b9-946d-a57749da073d
title: Eliminar una aplicación COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da685e5a7ae7590fcc247caa765d49dc34d076e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423399"
---
# <a name="deleting-a-com-application"></a>Eliminar una aplicación COM+

A medida que las aplicaciones existentes se hacen obsoletas o ya no se usan, puede que tenga que quitarlas.

**Para eliminar una aplicación COM+**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, seleccione el equipo para el que desea eliminar una aplicación.

2.  Abra la carpeta **aplicaciones com+** del equipo especificado para mostrar todas las aplicaciones.

3.  Seleccione la aplicación que desea quitar.

4.  Si seleccionó una aplicación de servidor, cierre la aplicación. Para cerrar una aplicación, selecciónela en la herramienta administrativa Servicios de componentes, haga clic con el botón secundario y, a continuación, haga clic en **apagar**. Si seleccionó una aplicación de biblioteca, asegúrese de que todos los procesos que usan actualmente esta aplicación de biblioteca están apagados.

5.  En el menú **acción** , haga clic en **eliminar**. También puede hacer clic con el botón secundario en el nombre de la aplicación y, a continuación, hacer clic en **eliminar**. También puede eliminar una aplicación seleccionándola en la herramienta administrativa Servicios de componentes y presionando la tecla **Supr** , o bien puede seleccionar la aplicación, hacer clic con el botón secundario y, a continuación, hacer clic en **eliminar**.

6.  Haga clic en **sí** cuando se le pida que confirme la acción.

Además, si una aplicación de servidor o proxy de aplicación se ha instalado en un equipo con Windows Installer (como se describe en "instalación de aplicaciones COM+" en la guía de administración de servicios de componentes), puede eliminarlo mediante la utilidad agregar o quitar programas del panel de control de Microsoft Windows. O bien, puede eliminar un proxy de aplicación o aplicación de servidor instalado mediante el uso de la sintaxis de la línea de comandos de Windows Installer:

**msiexec-x nombre de** *aplicación \_ * * *. msi**

Estos métodos son especialmente útiles para eliminar aplicaciones COM+ en equipos cliente que no ejecuten la herramienta administrativa Servicios de componentes.

Al eliminar la aplicación, también se eliminan los componentes contenidos en la aplicación. Si estos componentes dependen de recursos adicionales (conexiones de bases de datos, archivos de datos o texto, configuración de raíz virtual de IIS, etc.), estos recursos se deben quitar a través de mecanismos distintos de la herramienta administrativa Servicios de componentes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Copiar componentes](copying-components.md)
</dt> <dt>

[Crear una nueva aplicación COM+](creating-a-new-com--application.md)
</dt> <dt>

[Importar componentes](importing-components.md)
</dt> <dt>

[Instalación de nuevos componentes](installing-new-components.md)
</dt> <dt>

[Mover componentes](moving-components.md)
</dt> <dt>

[Quitar un componente de una aplicación COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



