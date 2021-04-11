---
description: Comandos
ms.assetid: f579745a-5327-4c8b-bfa7-fe81d9657a3b
title: Comandos (API de WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974c6b2b68949e53ae778ed56adcfcb10d2edd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275348"
---
# <a name="commands-wpd-api"></a>Comandos (API de WPD)

La aplicación cliente y el controlador se comunican mediante los comandos que se envían desde el cliente (a través de la API de dispositivos portátiles de Windows) al controlador (a través del marco de User-Mode driver). Un comando puede o no incluir un parámetro y puede devolver o no un resultado. Un cliente puede enviar un comando explícitamente, llamando al método [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) o al método **IPortableDeviceService: SendCommand** , o implícitamente, mediante una llamada a cualquiera de los métodos de las interfaces de cliente. Algunos comandos solo se pueden enviar explícitamente; Estos se indican en la documentación del comando. Las páginas de referencia de comandos describen el propósito de un comando, así como los parámetros que espera recibir y los parámetros que se espera que devuelva.

Un comando se identifica mediante una estructura **PROPERTYKEY** . Se compone de dos partes: una parte GUID (el miembro *fmtid* ) y una parte DWORD (el miembro *PID* ). La parte del GUID se usa para indicar la categoría a la que pertenece el comando (los comandos relacionados pertenecen a la misma categoría y, por tanto, tendrán el mismo *fmtid*). La parte DWORD indica el identificador del comando y se usa para distinguir los comandos individuales dentro de una categoría de comandos (los valores de *PID* para los comandos de la misma categoría serán diferentes).

En la tabla siguiente se enumeran las categorías de comandos que define Windows portable Devices. Los fabricantes de dispositivos pueden definir sus propios comandos mediante la creación de sus propios identificadores de comando y categorías de comandos. Sin embargo, un fabricante no debe agregar comandos a las categorías que se enumeran a continuación, ya que están reservadas por Microsoft.

**Categorías de comandos**



| Categoría de comando                         | Descripción                                                                                                                             |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **\_categoría \_ común de WPD**                | Comandos comunes a todos los objetos y dispositivos.                                                                                    |
| **\_categorías de \_ dispositivos de categoría de WPD \_**         | Comandos que se usan para recuperar información opcional del dispositivo que se puede usar para mejorar la experiencia del usuario final.                         |
| **\_SMS categoría de WPD \_**                   | Comandos que se usan para dispositivos que admiten la funcionalidad de servicio de mensajes cortos (SMS), que normalmente se expone en teléfonos móviles. |
| **\_captura de \_ \_ imagen \_ de la categoría de WPD** | Comandos que se usan para los dispositivos que admiten la captura de imágenes.                                                                    |
| **\_almacenamiento de categorías de WPD \_**               | Comandos que se usan para los objetos funcionales de almacenamiento.                                                                                  |



 

Los comandos específicos definidos para cada uno de estos tipos se proporcionan en las tablas siguientes, organizadas por tipo de comando.

**\_Categoría común de categoría de WPD \_**



| Get-Help                                                                                | Descripción        |
|----------------------------------------------------------------------------------------|--------------------|
| [**\_dispositivo de \_ \_ restablecimiento común de comandos \_ de WPD**](wpd-command-common-reset-device-command.md) | Restablece el dispositivo. |



 

**Categoría \_ de \_ sugerencias de dispositivo de categoría de WPD \_**



| Get-Help                                                                                                              | Descripción                                                                      |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**las \_ sugerencias de dispositivo de comandos WPD \_ obtienen la \_ \_ \_ Ubicación del contenido \_**](wpd-command-device-hints-get-content-location-command.md) | Recupera los identificadores de objeto de carpetas que pueden contener un objeto de un tipo especificado. |



 

**Categoría de almacenamiento de \_ categoría de WPD \_**



| Get-Help                                                                     | Descripción                                                         |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**expulsión del almacenamiento de comandos de WPD \_ \_ \_**](wpd-command-storage-eject-command.md)   | Expulsa un medio de almacenamiento que el controlador puede expulsar de forma remota. |
| [**\_formato de \_ almacenamiento de comandos de WPD \_**](wpd-command-storage-format-command.md) | Da formato a un objeto funcional de almacenamiento en el dispositivo.                  |



 

**\_Categoría de SMS categoría de WPD \_**



| Get-Help                                                         | Descripción                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| [**comando de WPD \_ \_ SMS \_ send**](wpd-command-sms-send-command.md) | Inicia el envío de un mensaje SMS mediante un objeto funcional de SMS. |



 

**Categoría \_ de \_ \_ captura de imagen \_ de la categoría de WPD**



| Get-Help                                                                                                   | Descripción                                                         |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**\_Inicio de \_ \_ captura de \_ imagen \_ de comando de WPD**](wpd-command-still-image-capture-initiate-command.md) | Inicia una captura de imagen continua mediante un objeto funcional de imagen fija. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 



