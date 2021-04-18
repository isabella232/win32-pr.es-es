---
description: El control WMI es un complemento MMC que se encuentra en el panel de control y se usa para establecer la seguridad del espacio de nombres WMI manualmente en un equipo local. También puede establecer el espacio de nombres predeterminado para el scripting.
ms.assetid: 87c23919-c482-4278-b005-894a8ac21da4
ms.tgt_platform: multiple
title: Establecer la seguridad del espacio de nombres con el control WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e8b6ed7c45b6b0d107f7f4e4b92f31f504900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707269"
---
# <a name="setting-namespace-security-with-the-wmi-control"></a>Establecer la seguridad del espacio de nombres con el control WMI

El control WMI es un complemento MMC que se encuentra en el **Panel de control** y se usa para establecer la seguridad del espacio de nombres WMI manualmente en un equipo local. También puede establecer el espacio de nombres predeterminado para el scripting.


En el procedimiento siguiente se describe cómo localizar el control WMI.

**Para buscar el control WMI**

1.  En el **Panel de control**, haga doble clic en **herramientas administrativas**.
2.  En la ventana **Herramientas administrativas**, haga doble clic en **Administración de equipos**.
3.  En la ventana **Administración de equipos** , expanda el árbol **servicios y aplicaciones** y haga doble clic en el **control WMI**.
4.  Haga clic con el botón secundario en el icono **control WMI** y seleccione **propiedades**.

En el procedimiento siguiente se describe cómo usar el control WMI para configurar la seguridad de un espacio de nombres como una plantilla y, a continuación, obtener mediante programación la configuración de seguridad para establecer la seguridad de otros espacios de nombres.

**Para establecer la seguridad del espacio de nombres con el control WMI**

1.  Cree un nuevo espacio de nombres mediante el código de Managed Object Format (MOF).
2.  Ejecute el control WMI para establecer la seguridad en el nuevo espacio de nombres. En el menú **Inicio** , haga clic en **Ejecutar** y escriba **Wmimgmt. msc** o vea [localizar el control WMI](#).
3.  En el panel **control WMI** , haga clic con el botón secundario en **control WMI**, seleccione **propiedades** y, a continuación, seleccione la pestaña **seguridad** .
4.  Navegue al nuevo espacio de nombres, haga clic en **seguridad** y, a continuación, configure los grupos y permisos para el espacio de nombres.

También puede usar Instrumental de administración de Windows Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) para establecer la seguridad de los espacios de nombres. Para obtener más información, vea [**WMIC**](wmic.md).

## <a name="setting-the-default-namespace-for-scripts"></a>Establecer el espacio de nombres predeterminado para los scripts

Si un script no se conecta explícitamente a un espacio de nombres al conectarse a WMI, WMI utiliza el espacio de nombres predeterminado especificado en este control. El valor predeterminado también se encuentra en la entrada del registro de la siguiente manera:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         WBEM
            Scripting
               Default
                  Namespace
```

Dado que el espacio de nombres predeterminado es fácil de cambiar, ya sea con este control o mediante programación llamando a los métodos de [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), especifique el espacio de nombres al conectarse a WMI a través del [moniker](constructing-a-moniker-string.md) o llamadas a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md). Para obtener más información, consulte [crear un script WMI](creating-a-wmi-script.md) .

**Para establecer el espacio de nombres predeterminado para los scripts**

1.  En la ventana **propiedades de control WMI** , elija la pestaña **Opciones avanzadas** .
2.  Haga clic en el botón **cambiar** y seleccione el espacio de nombres para establecer el valor predeterminado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de descriptores de seguridad de espacios de nombres](setting-namespace-security-descriptors.md)
</dt> </dl>

 

 
