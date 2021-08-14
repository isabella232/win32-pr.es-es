---
description: Windows Dispositivos portátiles admite las siguientes propiedades misceláneas.
ms.assetid: 0f2a5684-a94f-4a51-8f72-527204e4ebfa
title: Propiedades misceláneas (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Miscellaneous
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bdc093d877a180f6c7072ff9365e96edfe7d9e2c006fdcb745c58e92df3b179f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704435"
---
# <a name="miscellaneous-properties"></a>Propiedades misceláneas

Windows Dispositivos portátiles admite las siguientes propiedades misceláneas.



| Propiedad                                       | VarType         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **OPCIÓN DE API DE WPD \_ \_ USE CLEAR DATA \_ \_ \_ \_ STREAM** | **VT \_ BOOL**    | Valor booleano que especifica si el flujo de datos creado para la transferencia de datos estará claro, es decir, DRM no está implicado. Los clientes pueden establecer esta opción agregándole a las propiedades de objeto pasadas a [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).<br/>                                                                                                                                                   |
| **VERSIÓN DEL \_ SERVICIO \_ WPD**                      | **VT \_ LPWSTR**  | Cadena que especifica la versión de implementación de un servicio de dispositivo determinado.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **TIPOS DE \_ CONTENIDO DE \_ CARPETA WPD \_ \_ PERMITIDOS**       | **VT \_ UNKNOWN** | Valor que especifica los tipos de objeto que pueden ser elementos secundarios directos de esta carpeta. Las carpetas secundarias pueden tener diferentes funcionalidades. Esta propiedad es un [**IPortableDevicePropVariantCollection que**](iportabledevicepropvariantcollection.md) contiene valores \_ CLSID de VT que especifican los tipos de objeto permitidos.<br/> Para obtener una lista de los tipos de objeto definidos por Windows portables, vea [Requirements for Objects](requirements-for-objects.md).<br/>                                         |
| **CATEGORÍA DE OBJETOS \_ \_ FUNCIONALES DE \_ WPD**          | **VT \_ CLSID**   | Valor que especifica la categoría funcional del objeto.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **PERFILES DE \_ INFORMACIÓN \_ DE REPRESENTACIÓN \_ DE WPD**      | **VT \_ UNKNOWN** | [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) que contiene varias interfaces [**IPortableDeviceValues,**](iportabledevicevalues.md) cada una de las cuales contiene la configuración de propiedades de un perfil que el objeto admite.                                                                                                                                                                                                                                            |
| **NOMBRE PARA MOSTRAR \_ DE LA UBICACIÓN DE LA SUGERENCIA DE OBJETO \_ \_ \_ \_ WPD** | **VT \_ LPWSTR**  | Si un objeto es una ubicación de sugerencia, esta propiedad indica el nombre específico de la sugerencia que se va a mostrar al usuario en lugar del nombre del objeto. Los controladores pueden especificar sugerencias de ubicación para varios tipos de objeto. Estas son las ubicaciones de almacenamiento preferidas para las carpetas que tienen un tipo de objeto determinado. Un equivalente sería la carpeta Mis imágenes para los archivos de imagen de Windows. Si esta propiedad no existe, normalmente se [usa WPD \_ OBJECT \_ NAME](object-properties.md) en su lugar.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




