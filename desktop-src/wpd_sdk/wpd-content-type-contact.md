---
description: CONTACTO DE \_ TIPO DE \_ CONTENIDO WPD \_
ms.assetid: 3ff6191f-d3c0-4bd3-946e-c3fbf68f368c
title: WPD_CONTENT_TYPE_CONTACT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8354aa444f476e7c0b64d2e3d14d474c6eea02f90e8313c20073db2d0368fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083339"
---
# <a name="wpd_content_type_contact"></a>CONTACTO DE \_ TIPO DE \_ CONTENIDO WPD \_

Un objeto que describe su tipo como WPD \_ CONTENT TYPE CONTACT representa los datos de contacto \_ \_ personales.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad                                                                                                                   | Obligatorio u opcional                                                           |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ DE \_ WPD](object-properties.md)                                                                          | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación. |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                           | Obligatorio.                                                                      |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                                      | Obligatorio si el objeto representa un archivo.                                      |
| [WPD \_ OBJECT \_ PERSISTENT \_ UNIQUE \_ ID](object-properties.md)                                    | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación. |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                                  | Obligatorio.                                                                      |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                                     | Obligatorio.                                                                      |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                              | Obligatorio si el objeto está oculto.                                              |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                              | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).          |
| [TAMAÑO DEL OBJETO \_ WPD \_](object-properties.md)                                                                      | Obligatorio si el objeto tiene al menos un recurso.                              |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)                                        | Obligatorio si el objeto representa un archivo.                                      |
| [OBJETO WPD \_ \_ NO \_ CONSUMIBLE](object-properties.md)                                                 | Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo.          |
| [REFERENCIAS DE OBJETOS \_ WPD \_](object-properties.md)                                                          | Obligatorio si el objeto tiene referencias a otros objetos.                        |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                              | Opcional.                                                                      |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                               | Opcional.                                                                      |
| [EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM](object-properties.md)                                            | Obligatorio si el objeto está protegido por la tecnología DRM.                         |
| [FECHA DE CREACIÓN \_ DEL \_ OBJETO WPD \_](object-properties.md)                                                     | Opcional.                                                                      |
| [FECHA DE MODIFICACIÓN \_ DEL OBJETO \_ WPD \_](object-properties.md)                                                   | Se recomienda su uso.                                                                   |
| [FECHA DE CREACIÓN \_ DEL OBJETO \_ \_ WPD](object-properties.md)                                                   | Opcional.                                                                      |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)                                                                          | Se recomienda si otro objeto hace referencia al objeto.                     |
| [IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD](object-properties.md)               | Opcional.                                                                      |
| [WPD \_ OBJECT \_ GENERATE \_ THUMBNAIL \_ FROM \_ RESOURCE](object-properties.md)           | Opcional.                                                                      |
| [NOMBRE PARA MOSTRAR \_ DE CONTACTO \_ DE WPD \_](contact-properties.md)                                                  | Obligatorio.                                                                      |
| [EL OBJETO \_ WPD \_ PUEDE \_ ELIMINAR](object-properties.md)                                                                               | Obligatorio si no se puede eliminar el objeto.                                      |
| [CONFIGURACIÓN REGIONAL \_ DEL LENGUAJE DE OBJETOS \_ \_ WPD](object-properties.md)                                                                          | Opcional.                                                                      |
| [NOMBRE PARA MOSTRAR \_ DE CONTACTO \_ DE WPD \_](contact-properties.md)                                                                           | Obligatorio.                                                                      |
| [NOMBRE DEL CONTACTO DE WPD \_ \_ \_](contact-properties.md)                                                      | Se recomienda su uso.                                                                   |
| [NOMBRES \_ INTERMEDIOS DE CONTACTO DE WPD \_ \_](contact-properties.md)                                                  | Se recomienda su uso.                                                                   |
| [NOMBRE DEL CONTACTO DE WPD \_ \_ \_](contact-properties.md)                                                        | Se recomienda su uso.                                                                   |
| [PREFIJO DE CONTACTO DE WPD \_ \_](contact-properties.md)                                                               | Se recomienda su uso.                                                                   |
| [SUFIJO DE \_ CONTACTO WPD \_](contact-properties.md)                                                               | Se recomienda su uso.                                                                   |
| [NOMBRE FONÉTICO DE CONTACTO DE WPD \_ \_ \_ \_](contact-properties.md)                                   | Opcional.                                                                      |
| [WPD \_ CONTACT \_ PHONETIC LAST NAME (APELLIDOS \_ FONÉTICOS DE CONTACTO DE WPD) \_](contact-properties.md)                                     | Opcional.                                                                      |
| [DIRECCIÓN POSTAL COMPLETA PERSONAL DE CONTACTO \_ \_ \_ \_ DE \_ WPD](contact-properties.md)                | Se recomienda su uso.                                                                   |
| [WPD \_ CONTACT \_ PERSONAL \_ POSTAL \_ ADDRESS \_ LINE1](contact-properties.md)              | Opcional.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ POSTAL \_ ADDRESS \_ LINE2](contact-properties.md)              | Opcional.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ POSTAL \_ ADDRESS \_ CITY](contact-properties.md)                | Opcional.                                                                      |
| [REGIÓN DE DIRECCIÓN POSTAL PERSONAL DE CONTACTO \_ \_ \_ \_ DE \_ WPD](contact-properties.md)            | Opcional.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ POSTAL \_ ADDRESS \_ POSTAL \_ CODE](contact-properties.md) | Opcional.                                                                      |
| [PAÍS DE LA DIRECCIÓN POSTAL PERSONAL DE CONTACTO \_ \_ \_ \_ DE \_ WPD](contact-properties.md)          | Opcional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ FULL \_ POSTAL \_ ADDRESS](contact-properties.md)                | Opcional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ POSTAL \_ ADDRESS \_ LINE1](contact-properties.md)              | Opcional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ POSTAL \_ ADDRESS \_ LINE2](contact-properties.md)              | Opcional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ POSTAL \_ ADDRESS \_ CITY](contact-properties.md)                | Opcional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ POSTAL \_ ADDRESS \_ REGION](contact-properties.md)            | Opcional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ POSTAL \_ ADDRESS \_ POSTAL \_ CODE](contact-properties.md) | Opcional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ POSTAL \_ ADDRESS \_ COUNTRY](contact-properties.md)          | Opcional.                                                                      |
| [CONTACTO DE WPD \_ CON OTRA DIRECCIÓN POSTAL \_ \_ \_ \_ COMPLETA](contact-properties.md)                      | Opcional.                                                                      |
| [WPD \_ CONTACT \_ OTHER \_ POSTAL \_ ADDRESS \_ LINE1](contact-properties.md)                    | Opcional.                                                                      |
| [WPD \_ CONTACT \_ OTHER \_ POSTAL \_ ADDRESS \_ LINE2](contact-properties.md)                    | Opcional.                                                                      |
| [WPD \_ CONTACT \_ OTHER \_ POSTAL \_ ADDRESS \_ CITY](contact-properties.md)                      | Opcional.                                                                      |
| [WPD \_ CONTACT \_ OTHER \_ POSTAL \_ ADDRESS \_ REGION](contact-properties.md)                  | Opcional.                                                                      |
| [WPD \_ CONTACT \_ OTHER \_ POSTAL \_ ADDRESS \_ POSTAL \_ CODE](contact-properties.md)       | Opcional.                                                                      |
| [WPD \_ CONTACT \_ OTHER \_ POSTAL \_ ADDRESS \_ POSTAL \_ COUNTRY](contact-properties.md) | Opcional.                                                                      |
| [DIRECCIÓN DE CORREO ELECTRÓNICO \_ PRINCIPAL DE CONTACTO DE \_ \_ \_ WPD](contact-properties.md)                               | Se recomienda su uso.                                                                   |
| [CORREO ELECTRÓNICO PERSONAL \_ DE CONTACTO \_ DE \_ WPD](contact-properties.md)                                              | Opcional.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ EMAIL2](contact-properties.md)                                            | Opcional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ EMAIL](contact-properties.md)                                              | Opcional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ EMAIL2](contact-properties.md)                                            | Opcional.                                                                      |
| [CONTACTO DE WPD \_ \_ CON OTROS CORREOS \_ ELECTRÓNICOS](contact-properties.md)                                                  | Opcional.                                                                      |
| [TELÉFONO PRINCIPAL \_ DE CONTACTO \_ DE WPD \_](contact-properties.md)                                                | Se recomienda su uso.                                                                   |
| [TELÉFONO PERSONAL \_ DE CONTACTO \_ DE WPD \_](contact-properties.md)                                              | Opcional.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ PHONE2](contact-properties.md)                                            | Opcional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ PHONE](contact-properties.md)                                              | Opcional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ PHONE2](contact-properties.md)                                            | Opcional.                                                                      |
| [WPD \_ CONTACT \_ MOBILE \_ PHONE](contact-properties.md)                                                  | Opcional.                                                                      |
| [WPD \_ CONTACT \_ MOBILE \_ PHONE2](contact-properties.md)                                                | Opcional.                                                                      |
| [FAX PERSONAL \_ DE CONTACTO \_ DE WPD \_](contact-properties.md)                                                  | Opcional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ FAX](contact-properties.md)                                                  | Opcional.                                                                      |
| [WPD \_ CONTACT \_ PAGER](contact-properties.md)                                                                 | Opcional.                                                                      |
| [CONTACTO DE WPD \_ \_ CON OTROS \_ TELÉFONOS](contact-properties.md)                                                  | Opcional.                                                                      |
| [DIRECCIÓN WEB PRINCIPAL \_ \_ DE CONTACTO DE \_ \_ WPD](contact-properties.md)                                   | Se recomienda su uso.                                                                   |
| [DIRECCIÓN WEB \_ PERSONAL DE CONTACTO DE \_ \_ \_ WPD](contact-properties.md)                                 | Opcional.                                                                      |
| [DIRECCIÓN WEB DE \_ CONTACTO \_ DE \_ WPD PARA \_ EMPRESAS](contact-properties.md)                                 | Opcional.                                                                      |
| [WPD \_ CONTACT \_ INSTANT \_ MESSENGER](contact-properties.md)                                        | Recomendado                                                                    |
| [WPD \_ CONTACT \_ INSTANT \_ MESSENGER2](contact-properties.md)                                      | Opcional.                                                                      |
| [WPD \_ CONTACT \_ INSTANT \_ MESSENGER3](contact-properties.md)                                      | Opcional.                                                                      |
| [WPD \_ CONTACT \_ COMPANY \_ NAME](contact-properties.md)                                                  | Opcional.                                                                      |
| [NOMBRE DE LA COMPAÑÍA FONÉTICA DE CONTACTO \_ \_ DE \_ \_ WPD](contact-properties.md)                               | Opcionales                                                                       |
| [ROL CONTACTO \_ DE \_ WPD](contact-properties.md)                                                                   | Opcional.                                                                      |
| [WPD \_ CONTACT \_ BIRTHDATE](contact-properties.md)                                                         | Opcional.                                                                      |
| [FAX PRINCIPAL \_ DE CONTACTO \_ DE WPD \_](contact-properties.md)                                                                            | Opcional.                                                                      |
| [CONTACTO DE WPD \_ \_ CON EL GOBIERNO](contact-properties.md)                                                                                  | Opcional.                                                                      |
| [WPD \_ CONTACT \_ CHILDREN](contact-properties.md)                                                                                | Opcional.                                                                      |
| [ASISTENTE DE \_ CONTACTO DE \_ WPD](contact-properties.md)                                                                               | Opcional.                                                                      |
| [FECHA DE ANIVERSARIO \_ DE CONTACTO \_ DE \_ WPD](contact-properties.md)                                                                       | Opcional.                                                                      |
| [WPD \_ CONTACT \_ LORÓN](contact-properties.md)                                                                                | Opcional.                                                                      |
| [NOTAS DE INFORMACIÓN \_ \_ COMUNES DE \_ WPD](object-properties.md)                                                                        | Opcional.                                                                      |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos suelen incluir los siguientes recursos.



| Nombre de recurso                                                       | Obligatorio u opcional       | Descripción                        |
|---------------------------------------------------------------------|----------------------------|------------------------------------|
| [**WPD \_ RESOURCE \_ DEFAULT**](wpd-resource-default.md)              | Opcional.                  | Contiene los datos de contacto.         |
| [**WPD \_ RESOURCE \_ CONTACT \_ PHOTO**](wpd-resource-contact-photo.md) | Recomendado, si está disponible. | Contiene una imagen del contacto. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



