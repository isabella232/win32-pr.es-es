---
description: A medida que las aplicaciones existentes tienen fecha o ya no se usan, es posible que deba quitarlas.
ms.assetid: 5cce94c9-8eff-40b9-946d-a57749da073d
title: Eliminación de una aplicación COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da685e5a7ae7590fcc247caa765d49dc34d076e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466971"
---
# <a name="deleting-a-com-application"></a>Eliminación de una aplicación COM+

A medida que las aplicaciones existentes tienen fecha o ya no se usan, es posible que deba quitarlas.

**Para eliminar una aplicación COM+**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, seleccione el equipo para el que desea eliminar una aplicación.

2.  Abra la **carpeta Aplicaciones COM+** del equipo especificado para mostrar todas las aplicaciones.

3.  Seleccione la aplicación que desea quitar.

4.  Si seleccionó una aplicación de servidor, cierre la aplicación. Para apagar una aplicación, selecciónelo en la herramienta administrativa Servicios de componentes, haga clic con el botón derecho y, a continuación, haga clic **en Apagar.** Si seleccionó una aplicación de biblioteca, asegúrese de que todos los procesos que usan actualmente esta aplicación de biblioteca estén apagados.

5.  En el **menú Acción** , haga clic **en Eliminar.** También puede hacer clic con el botón derecho en el nombre de la aplicación y, a continuación, hacer clic **en Eliminar**. También puede eliminar una aplicación si la selecciona en la  herramienta administrativa Servicios de componentes y presiona la tecla Eliminar, o bien puede seleccionar la aplicación, hacer clic con el botón derecho y, a continuación, hacer clic en **Eliminar**.

6.  Haga **clic en Sí** cuando se le pida que confirme la acción.

Además, si se ha instalado una aplicación de servidor o un proxy de aplicación en un equipo mediante el instalador de Windows (como se describe en "Instalación de aplicaciones COM+" en la Guía de administración de servicios de componentes), puede eliminarlo a través de la utilidad Agregar o quitar programas en Microsoft Windows Panel de control. O bien, puede eliminar una aplicación de servidor instalada o un proxy de aplicación mediante la sintaxis de la línea de comandos Windows Installer:

**msiexec -x** *nombre de la \_ aplicación,.msi**

Estos métodos son especialmente útiles para eliminar aplicaciones COM+ en equipos cliente que no ejecutan la herramienta administrativa Servicios de componentes.

Al eliminar la aplicación también se eliminan los componentes contenidos en la aplicación. Si estos componentes dependen de recursos adicionales (conexiones de base de datos, archivos de datos o de texto, configuración raíz virtual de IIS, entre otros), estos recursos se deben quitar mediante mecanismos distintos de la herramienta administrativa Servicios de componentes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Copiar componentes](copying-components.md)
</dt> <dt>

[Creación de una nueva aplicación COM+](creating-a-new-com--application.md)
</dt> <dt>

[Importar componentes](importing-components.md)
</dt> <dt>

[Instalación de nuevos componentes](installing-new-components.md)
</dt> <dt>

[Mover componentes](moving-components.md)
</dt> <dt>

[Quitar un componente de una aplicación COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



