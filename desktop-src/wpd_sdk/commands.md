---
description: Comandos
ms.assetid: f579745a-5327-4c8b-bfa7-fe81d9657a3b
title: Comandos (API de WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a723e9eff52bf0b0b301d1fba672db5887afebef701a312786aeafb4decb733f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431118"
---
# <a name="commands-wpd-api"></a>Comandos (API de WPD)

La aplicación cliente y el controlador se comunican mediante comandos que se envían desde el cliente (a través de la API de dispositivo portátil de Windows) al controlador (a través de User-Mode Driver Framework). Un comando puede incluir o no un parámetro y puede o no devolver un resultado. Un cliente puede enviar un comando explícitamente, llamando al método [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) o al método **IPortableDeviceService:SendCommand,** o implícitamente, llamando a cualquiera de los métodos de las interfaces de cliente. Solo se pueden enviar algunos comandos explícitamente; se anotan en la documentación del comando. Las páginas de referencia de comandos describen el propósito de un comando, así como los parámetros que espera recibir y los parámetros que se espera que devuelva.

Un comando se identifica mediante una **estructura PROPERTYKEY.** Se trata de dos partes: una parte GUID (el miembro *fmtid)* y una parte DWORD (el *miembro pid).* La parte GUID se usa para indicar la categoría a la que pertenece el comando (los comandos relacionados pertenecen a la misma categoría y, por tanto, tendrán el mismo *fmtid*). La parte DWORD indica el identificador de comando y se usa para distinguir los comandos individuales dentro de una categoría de comandos (los valores *pid* de los comandos de la misma categoría serán diferentes).

En la tabla siguiente se enumeran las categorías de comandos que Windows Portable Devices define. Los fabricantes de dispositivos pueden definir sus propios comandos mediante la creación de sus propias categorías de comandos e iDs de comando. Sin embargo, un fabricante no debe agregar comandos a las categorías enumeradas a continuación, ya que microsoft los reserva.

**Categorías de comandos**



| Categoría de comando                         | Descripción                                                                                                                             |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **CATEGORÍA WPD \_ \_ COMÚN**                | Comandos que son comunes a todos los objetos y dispositivos.                                                                                    |
| **SUGERENCIAS DE \_ DISPOSITIVO \_ DE CATEGORÍA WPD \_**         | Comandos que se usan para recuperar información opcional del dispositivo que se puede usar para mejorar la experiencia del usuario final.                         |
| **SMS DE \_ CATEGORÍA WPD \_**                   | Comandos que se usan para dispositivos que admiten la funcionalidad de servicio de mensajes cortos (SMS), que normalmente se expone en teléfonos móviles. |
| **CAPTURA DE IMÁGENES \_ DE LA CATEGORÍA \_ WPD \_ \_** | Comandos que se usan para dispositivos que admiten la captura de imágenes fijas.                                                                    |
| **ALMACENAMIENTO DE \_ CATEGORÍA WPD \_**               | Comandos que se usan para los objetos funcionales de almacenamiento.                                                                                  |



 

Los comandos específicos que se definen para cada uno de estos tipos se dan en las tablas siguientes, organizadas por tipo de comando.

**CATEGORÍA WPD \_ \_ CATEGORÍA COMÚN**



| Get-Help                                                                                | Descripción        |
|----------------------------------------------------------------------------------------|--------------------|
| [**COMANDO WPD \_ \_ RESTABLECIMIENTO \_ COMÚN DEL \_ DISPOSITIVO**](wpd-command-common-reset-device-command.md) | Restablece el dispositivo. |



 

**CATEGORÍA WPD \_ \_ Categoría \_ SUGERENCIAS DE DISPOSITIVO**



| Get-Help                                                                                                              | Descripción                                                                      |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**SUGERENCIAS DE DISPOSITIVO DEL COMANDO WPD \_ PARA OBTENER LA UBICACIÓN DEL \_ \_ \_ \_ \_ CONTENIDO**](wpd-command-device-hints-get-content-location-command.md) | Recupera los iDs de objeto de las carpetas que pueden contener un objeto de un tipo especificado. |



 

**Categoría DE \_ ALMACENAMIENTO DE CATEGORÍA \_ WPD**



| Get-Help                                                                     | Descripción                                                         |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**EXPULSIÓN DE \_ ALMACENAMIENTO DE \_ COMANDOS WPD \_**](wpd-command-storage-eject-command.md)   | Expulsa un medio de almacenamiento que el controlador puede expulsar de forma remota. |
| [**FORMATO DE ALMACENAMIENTO \_ DE COMANDOS \_ \_ WPD**](wpd-command-storage-format-command.md) | Da formato a un objeto funcional de almacenamiento en el dispositivo.                  |



 

**CATEGORÍA WPD \_ Categoría \_ SMS**



| Get-Help                                                         | Descripción                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| [**ENVÍO DE \_ SMS DEL \_ COMANDO WPD \_**](wpd-command-sms-send-command.md) | Inicia el envío de un mensaje SMS mediante un objeto funcional de SMS. |



 

**CATEGORÍA WPD \_ CATEGORÍA STILL IMAGE CAPTURE \_ \_ \_ Category**



| Get-Help                                                                                                   | Descripción                                                         |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**COMANDO WPD \_ \_ STILL IMAGE CAPTURE \_ \_ \_ INITIATE**](wpd-command-still-image-capture-initiate-command.md) | Inicia una captura de imagen fija mediante un objeto funcional de imagen fija. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 



