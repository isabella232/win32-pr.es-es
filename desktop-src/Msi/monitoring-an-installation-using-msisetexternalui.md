---
description: Los autores de paquetes pueden supervisar los mensajes Windows Installer internos mediante la creación de una aplicación ejecutable que contiene un controlador de devolución de llamada para recibir los mensajes y la funcionalidad para iniciar una instalación.
ms.assetid: 0aa8a2d6-f519-4d87-a28f-a11cb546bff5
title: Supervisión de una instalación mediante MsiSetExternalUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9660b1454d7e4f3437da6dce41707a1516207d853510e8475837f31e60090b78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628576"
---
# <a name="monitoring-an-installation-using-msisetexternalui"></a>Supervisión de una instalación mediante MsiSetExternalUI

Los autores de paquetes pueden supervisar los mensajes Windows Installer internos mediante la creación de una aplicación ejecutable que contiene un controlador de devolución de llamada para recibir los mensajes y la funcionalidad para iniciar una instalación.

El controlador de devolución de llamada se ajusta al prototipo INSTALLUI HANDLER y se pasa un puntero a este controlador de devolución de llamada \_ a [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia). Una vez iniciada la instalación mediante una llamada a [**MsiInstallProduct,**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)el controlador de devolución de llamada se queda con los mensajes de instalación y el autor del paquete puede mostrar u omitir de forma selectiva cualquiera o todos estos mensajes.

Para obtener más información, vea Controlar mensajes de progreso mediante [MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md), Devolver valores de un controlador de [Interfaz de usuario](returning-values-from-an-external-user-interface-handler.md)externo y Analizar Windows [mensajes del instalador](parsing-windows-installer-messages.md).

Para obtener más información sobre el uso de un controlador externo basado en registros, vea Supervisar una instalación [mediante MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md).

 

 



