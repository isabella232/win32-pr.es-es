---
title: Control del contenido protegido en el proveedor de servicios
description: Control del contenido protegido en el proveedor de servicios
ms.assetid: 5c18c8ec-d579-41df-8c25-c143fb9cdbef
keywords:
- Windows Media Administrador de dispositivos,certificates
- Administrador de dispositivos,certificates
- guía de programación, certificados
- proveedores de servicios, certificados
- crear proveedores de servicios, certificados
- certificates
- Windows Contenido Administrador de dispositivos multimedia protegido por DRM
- Administrador de dispositivos contenido protegido por DRM
- guía de programación, contenido protegido por DRM
- proveedores de servicios, contenido protegido por DRM
- crear proveedores de servicios, contenido protegido por DRM
- Contenido protegido por DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d10cf9078cf9aaf631b65de968f01491a97781
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068514"
---
# <a name="handling-protected-content-in-the-service-provider"></a>Control del contenido protegido en el proveedor de servicios

Puede crear un proveedor de servicios que pueda enviar contenido protegido por DRM a un dispositivo basado en DRM de dispositivo portátil (PDDRM), pero no puede crear un proveedor de servicios que pueda enviar contenido protegido por DRM a dispositivos integrados en Windows Media DRM 10 para dispositivos portátiles. Estos dispositivos usan MTP y no puede crear su propio proveedor de servicios MTP.

El único paso adicional que debe realizar un proveedor de servicios para enviar material DRM a un dispositivo PDDRM es obtener un par de claves o certificados emitidos por Microsoft. Consulte [Herramientas de desarrollo](tools-for-development.md) para obtener información sobre dónde obtener este certificado o clave. Las licencias emitidas para estos dispositivos serán licencias simplificadas que solo admiten la reproducción sencilla del contenido comprado. no admitirán licencias que expiran en el tiempo. El proveedor de contenido seguro (proporcionado por Microsoft para archivos WMA/WMV) creará automáticamente esta licencia y se almacenará en el encabezado del archivo enviado al proveedor de servicios. No tendrá que realizar ningún paso especial para los archivos protegidos.

Después de enviar el archivo protegido, Windows Media Administrador de dispositivos llamará al proveedor de servicios para solicitar un archivo de almacenamiento de licencia especial del dispositivo. Windows Los Administrador de dispositivos agregarán una copia de la nueva licencia a este archivo y la devolverán al proveedor de servicios para que la devuelva al dispositivo. Sin embargo, incluso si el proveedor de servicios no encuentra o devuelve este archivo, el dispositivo todavía debe poder reproducir el archivo protegido mediante la copia de licencia en el encabezado de archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un proveedor de servicios**](creating-a-service-provider.md)
</dt> <dt>

[**Control de contenido protegido**](handling-protected-content.md)
</dt> </dl>

 

 




