---
description: Siga estas instrucciones para cubrir una instalación Windows Installer completa mediante una firma digital.
ms.assetid: e70eab94-4615-4a73-bccc-e16bd24551f6
title: Crear una instalación firmada completamente comprobada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e76bbfb77eab8b020cb1591847d2a36d09c96a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667038"
---
# <a name="authoring-a-fully-verified-signed-installation"></a>Crear una instalación firmada completamente comprobada

Puede usar estas instrucciones para cubrir una instalación Windows Installer completa mediante una firma digital.

Los autores de instalaciones de Windows Installer deben cumplir los siguientes pasos para asegurarse de que todas las partes de la instalación están tratadas por una firma digital:

-   Use archivos. cab internos, o bien use archivos. cab externos firmados y cree correctamente la tabla [MsiDigitalSignature](msidigitalsignature-table.md) y la [tabla MsiDigitalCertificate](msidigitalcertificate-table.md).
-   Use solo las acciones personalizadas almacenadas en el paquete o instaladas con el paquete.
-   Firme el paquete de instalación.
-   Incluya una [tabla MsiPatchCertificate](msipatchcertificate-table.md) en el paquete. Para habilitar la [revisión de control de cuentas de usuario (UAC)](user-account-control--uac--patching.md), esta tabla debe contener información utilizada para identificar los certificados de firmante que se usan para firmar revisiones digitalmente. La aplicación de revisiones de UAC permite al autor del paquete de instalación identificar revisiones firmadas digitalmente que los usuarios que no son administradores pueden aplicar en el futuro.

Para ver un ejemplo en el que se muestra cómo crear una instalación firmada mediante automatización, vea [crear una instalación firmada completamente comprobada mediante automatización](authoring-a-fully-verified-signed-installation-using-automation.md).

 

 



