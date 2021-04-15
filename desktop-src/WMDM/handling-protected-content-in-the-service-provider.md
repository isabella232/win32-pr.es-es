---
title: Control del contenido protegido en el proveedor de servicios
description: Control del contenido protegido en el proveedor de servicios
ms.assetid: 5c18c8ec-d579-41df-8c25-c143fb9cdbef
keywords:
- Windows Media Administrador de dispositivos, certificados
- Administrador de dispositivos, certificados
- Guía de programación, certificados
- proveedores de servicios, certificados
- crear proveedores de servicios, certificados
- certificates
- Windows Media Administrador de dispositivos, contenido protegido con DRM
- Administrador de dispositivos, contenido protegido con DRM
- Guía de programación, contenido protegido con DRM
- proveedores de servicios, contenido protegido con DRM
- creación de proveedores de servicios, contenido protegido con DRM
- Contenido protegido con DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d10cf9078cf9aaf631b65de968f01491a97781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695272"
---
# <a name="handling-protected-content-in-the-service-provider"></a>Control del contenido protegido en el proveedor de servicios

Puede crear un proveedor de servicios que pueda enviar contenido protegido con DRM a un dispositivo basado en DRM de dispositivo portátil (PDDRM), pero no puede crear un proveedor de servicios que pueda enviar contenido protegido con DRM a dispositivos basados en Windows Media DRM 10 para dispositivos portátiles. Estos dispositivos usan MTP y no puede crear su propio proveedor de servicios MTP.

El único paso adicional que un proveedor de servicios debe llevar a cabo para enviar material de DRM a un dispositivo PDDRM es obtener un par certificado/clave emitido por Microsoft. Consulte [herramientas de desarrollo](tools-for-development.md) para obtener información sobre dónde obtener este certificado o clave. Las licencias emitidas para estos dispositivos serán licencias simplificadas que solo admitan la reproducción simple del contenido adquirido. no admitirán licencias de expiración de tiempo. Esta licencia la creará el proveedor de contenido seguro (proporcionado por Microsoft para archivos WMA/WMV) y se almacenará en el encabezado del archivo que se envía al proveedor de servicios. No tendrá que realizar ningún paso especial para los archivos protegidos.

Después de enviar el archivo protegido, Windows Media Administrador de dispositivos llamará al proveedor de servicios para solicitar un archivo de almacenamiento de licencias especial del dispositivo. Windows Media Administrador de dispositivos agregará una copia de la nueva licencia a este archivo y lo devolverá al proveedor de servicios para devolverlo al dispositivo. Sin embargo, aunque el proveedor de servicios no encuentre o devuelva este archivo, el dispositivo todavía debe ser capaz de reproducir el archivo protegido mediante la copia de la licencia en el encabezado del archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un proveedor de servicios**](creating-a-service-provider.md)
</dt> <dt>

[**Control de contenido protegido**](handling-protected-content.md)
</dt> </dl>

 

 




