---
title: Referencia del controlador instalable
description: Referencia del controlador instalable
ms.assetid: 869b92f1-2711-4198-9911-3df1ebc58d5f
keywords:
- Windows referencia de controlador multimedia instalable
- multimedia, referencia del controlador instalable
- controladores instalables, referencia
- referencia del controlador instalable, acerca de
- referencia de los controladores instalables, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90475063f9d9211e841902fe73d2f09dc6130d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069528"
---
# <a name="installable-driver-reference"></a>Referencia del controlador instalable

Las funciones y los mensajes asociados a los controladores instalables se agrupan como se muestra a continuación.

## <a name="loading-and-unloading-drivers"></a>Carga y descarga de controladores

-   [GetDriverModuleHandle](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle)
-   [OpenDriver](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver)
-   [SendDriverMessage](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage)

## <a name="closedriver"></a>CloseDriver

-   [**DRV \_ CLOSE**](drv-close.md)
-   [**DESHABILITACIÓN DE DRV \_**](drv-disable.md)
-   [**HABILITACIÓN DE DRV \_**](drv-enable.md)
-   [**DRV \_ GRATIS**](drv-free.md)
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

 

 