---
title: Referencia del controlador instalable
description: Referencia del controlador instalable
ms.assetid: 869b92f1-2711-4198-9911-3df1ebc58d5f
keywords:
- Windows de controlador multimedia instalable
- multimedia, referencia de controladores instalables
- controladores instalables, referencia
- referencia del controlador instalable, acerca de
- referencia de los controladores instalables, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6dd2488f0b07805edbcdc90187309db2a04c9c0ced4f4b5b0af4e50bd983ca4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038645"
---
# <a name="installable-driver-reference"></a>Referencia del controlador instalable

Las funciones y los mensajes asociados a los controladores instalables se agrupan como se muestra a continuación.

## <a name="loading-and-unloading-drivers"></a>Carga y descarga de controladores

-   [GetDriverModuleHandle](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle)
-   [OpenDriver](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver)
-   [SendDriverMessage](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage)

## <a name="closedriver"></a>CloseDriver

-   [**DRV \_ CLOSE**](drv-close.md)
-   [**DRV \_ DISABLE**](drv-disable.md)
-   [**DRV \_ ENABLE**](drv-enable.md)
-   [**DRV \_ FREE**](drv-free.md)
-   [**CARGA \_ DE DRV**](drv-load.md)
-   [**DRV \_ OPEN**](drv-open.md)

## <a name="configuring-a-driver"></a>Configuración de un controlador

-   [**CONFIGURACIÓN \_ DE DRV**](drv-configure.md)
-   [**DRV \_ QUERYCONFIGURE**](drv-queryconfigure.md)
-   [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo)

## <a name="installing-a-driver"></a>Instalación de un controlador

-   [**INSTALACIÓN \_ DE DRV**](drv-install.md)
-   [**DRV \_ REMOVE**](drv-remove.md)

## <a name="driver-functions"></a>Funciones de controlador

-   [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc)
-   [DriverCallback](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback)
-   [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controladores instalables](installable-drivers.md)
</dt> </dl>

 

 