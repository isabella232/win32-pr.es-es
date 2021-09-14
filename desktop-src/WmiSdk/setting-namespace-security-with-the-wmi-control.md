---
description: El control WMI es un complemento MMC ubicado en el Panel de control y se usa para establecer la seguridad del espacio de nombres WMI manualmente en un equipo local. También puede establecer el espacio de nombres predeterminado para el scripting.
ms.assetid: 87c23919-c482-4278-b005-894a8ac21da4
ms.tgt_platform: multiple
title: Establecer la seguridad del espacio de nombres con el control WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e8b6ed7c45b6b0d107f7f4e4b92f31f504900
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073058"
---
# <a name="setting-namespace-security-with-the-wmi-control"></a>Establecer la seguridad del espacio de nombres con el control WMI

El control WMI es un complemento MMC ubicado en el Panel de control y se usa para establecer la seguridad del espacio de nombres WMI manualmente en un equipo local.  También puede establecer el espacio de nombres predeterminado para el scripting.


En el procedimiento siguiente se describe cómo buscar el control WMI.

**Para buscar el control WMI**

1.  En **la** Panel de control , haga doble clic en **Herramientas administrativas**.
2.  En la ventana **Herramientas administrativas**, haga doble clic en **Administración de equipos**.
3.  En la **ventana Administración de** equipos, expanda el árbol Servicios y **aplicaciones** y haga doble clic en el **Control WMI**.
4.  Haga clic con el botón derecho en **el icono Control WMI** y seleccione **Propiedades.**

En el procedimiento siguiente se describe cómo usar el control WMI para configurar la seguridad de un espacio de nombres como una plantilla y, a continuación, obtener mediante programación la configuración de seguridad para establecer la seguridad de otros espacios de nombres.

**Para establecer la seguridad del espacio de nombres con el control WMI**

1.  Cree un nuevo espacio de nombres mediante Managed Object Format (MOF).
2.  Ejecute el control WMI para establecer la seguridad en el nuevo espacio de nombres. En el **menú Inicio** , haga clic **en Ejecutar** y escriba **wmimgmt.msc** o vea [Buscar el control WMI](#).
3.  En el **panel Control WMI,** haga clic con el botón derecho **en Control WMI,** elija **Propiedades** y, a continuación, seleccione **la pestaña** Seguridad.
4.  Vaya al nuevo espacio de nombres, haga clic **en Seguridad** y, a continuación, configure grupos y permisos para el espacio de nombres.

También puede usar Windows Management Instrumentation Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) para establecer la seguridad del espacio de nombres. Para obtener más información, [**vea wmic**](wmic.md).

## <a name="setting-the-default-namespace-for-scripts"></a>Establecer el espacio de nombres predeterminado para scripts

Si un script no se conecta explícitamente a un espacio de nombres al conectarse a WMI, WMI usa el espacio de nombres predeterminado especificado en este control. El valor predeterminado también se encuentra en la entrada del Registro como se muestra a continuación:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         WBEM
            Scripting
               Default
                  Namespace
```

Dado que el espacio de nombres predeterminado es fácil de cambiar, ya sea con este control o mediante programación llamando a métodos de [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), especifique el espacio de nombres al conectarse a WMI mediante el [moniker](constructing-a-moniker-string.md) o las llamadas a [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md). Para obtener más información, vea [Crear un script WMI.](creating-a-wmi-script.md)

**Para establecer el espacio de nombres predeterminado para los scripts**

1.  En la **ventana Propiedades del control WMI,** elija la **pestaña** Avanzadas.
2.  Haga clic en **el botón** Cambiar y seleccione el espacio de nombres para crear el valor predeterminado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer descriptores de seguridad de espacio de nombres](setting-namespace-security-descriptors.md)
</dt> </dl>

 

 
