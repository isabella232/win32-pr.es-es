---
title: Referencia del controlador instalable
description: Referencia del controlador instalable
ms.assetid: 869b92f1-2711-4198-9911-3df1ebc58d5f
keywords:
- Windows multimedia, referencia del controlador instalable
- multimedia, referencia del controlador instalable
- Controladores instalables, referencia
- Referencia del controlador instalable, acerca de
- referencia de controladores instalables, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90475063f9d9211e841902fe73d2f09dc6130d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904530"
---
# <a name="installable-driver-reference"></a>Referencia del controlador instalable

Las funciones y los mensajes asociados a los controladores instalables se agrupan de la siguiente manera.

## <a name="loading-and-unloading-drivers"></a>Cargar y descargar controladores

-   [GetDriverModuleHandle](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle)
-   [OpenDriver](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver)
-   [SendDriverMessage](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage)

## <a name="closedriver"></a>CloseDriver

-   [**DRV \_ cerrar**](drv-close.md)
-   [**DRV \_ Disable**](drv-disable.md)
-   [**DRV ( \_ Habilitar)**](drv-enable.md)
-   [**DRV \_ gratis**](drv-free.md)
-   [**carga de DRV \_**](drv-load.md)
-   [**DRV \_ Open**](drv-open.md)

## <a name="configuring-a-driver"></a>Configuración de un controlador

-   [**configuración de DRV \_**](drv-configure.md)
-   [**DRV \_ QUERYCONFIGURE**](drv-queryconfigure.md)
-   [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo)

## <a name="installing-a-driver"></a>Instalación de un controlador

-   [**instalación de DRV \_**](drv-install.md)
-   [**DRV \_ Remove**](drv-remove.md)

## <a name="driver-functions"></a>Funciones de controlador

-   [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc)
-   [DriverCallback](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback)
-   [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controladores instalables](installable-drivers.md)
</dt> </dl>

 

 