---
description: Use estas directrices para cubrir una instalación completa Windows Installer mediante una firma digital.
ms.assetid: e70eab94-4615-4a73-bccc-e16bd24551f6
title: Creación de una instalación firmada totalmente verificada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d105b06e3f063d8cbeb1fac579beb12258b20062bf5cbae2cc6d08e9be6e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066185"
---
# <a name="authoring-a-fully-verified-signed-installation"></a>Creación de una instalación firmada totalmente verificada

Puede usar estas directrices para cubrir una instalación completa Windows Installer mediante una firma digital.

Los autores de Windows instalador deben cumplir lo siguiente para asegurarse de que todas las partes de la instalación están cubiertas por una firma digital:

-   Use archivos de contenedor internos o use archivos de contenedor externos firmados y cree correctamente la tabla [MsiDigitalSignature](msidigitalsignature-table.md) y [la tabla MsiDigitalCertificate](msidigitalcertificate-table.md).
-   Use solo acciones personalizadas almacenadas en el paquete o instaladas con el paquete.
-   Firme el paquete de instalación.
-   Incluya una [tabla MsiPatchCertificate](msipatchcertificate-table.md) en el paquete. Para habilitar la aplicación de revisiones de control de cuentas de usuario [(UAC),](user-account-control--uac--patching.md)esta tabla debe contener información que se usa para identificar los certificados de firmante usados para firmar revisiones digitalmente. La aplicación de revisiones de UAC permite al autor del paquete de instalación identificar las revisiones firmadas digitalmente que los usuarios que no son administradores pueden aplicar en el futuro.

Para obtener un ejemplo en el que se muestra cómo crear una instalación firmada mediante automatización, vea Creación de [una instalación firmada totalmente comprobada mediante Automation.](authoring-a-fully-verified-signed-installation-using-automation.md)

 

 



