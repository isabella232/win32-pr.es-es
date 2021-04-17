---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades varias.
ms.assetid: 0f2a5684-a94f-4a51-8f72-527204e4ebfa
title: Propiedades varias (PortableDevice. h)
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
ms.openlocfilehash: 6bc5f90bb04c2ee0d018d03ee07b6cd7436e6593
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670649"
---
# <a name="miscellaneous-properties"></a>Propiedades varias

Los dispositivos portátiles de Windows admiten las siguientes propiedades varias.



| Propiedad                                       | VarType         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **la opción de la API de WPD \_ \_ \_ usar \_ Clear \_ Data \_ Stream** | **VT \_ bool**    | Un valor booleano que especifica si el flujo de datos creado para la transferencia de datos será claro, es decir, DRM no está implicado. Los clientes pueden establecer esta opción agregándolas a las propiedades de objeto que se pasan a [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).<br/>                                                                                                                                                   |
| **\_versión del servicio WPD \_**                      | **VT \_ LPWStr**  | Cadena que especifica la versión de implementación de un servicio de dispositivo determinado.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **tipos de contenido de la carpeta de WPD \_ \_ \_ \_ permitidos**       | **VT \_ desconocido** | Valor que especifica los tipos de objeto que pueden ser elementos secundarios directos de esta carpeta. Las carpetas secundarias pueden tener diferentes capacidades. Esta propiedad es una [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contiene \_ los valores CLSID de VT que especifican los tipos de objeto permitidos.<br/> Para obtener una lista de tipos de objetos definidos por dispositivos portátiles de Windows, consulte [requisitos de objetos](requirements-for-objects.md).<br/>                                         |
| **\_categoría de \_ objeto \_ funcional de WPD**          | **VT \_ CLSID**   | Valor que especifica la categoría funcional del objeto.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **perfiles de información de representación de WPD \_ \_ \_**      | **VT \_ desconocido** | [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) que contiene varias interfaces [**IPortableDeviceValues**](iportabledevicevalues.md) , cada una de las cuales contiene los valores de propiedad de un perfil que admite el objeto.                                                                                                                                                                                                                                            |
| **nombre para mostrar de la ubicación de la \_ sugerencia de objeto WPD \_ \_ \_ \_** | **VT \_ LPWStr**  | Si un objeto es una ubicación de sugerencia, esta propiedad indica el nombre específico de la sugerencia que se va a mostrar al usuario en lugar del nombre del objeto. Los controladores pueden especificar sugerencias de ubicación para varios tipos de objeto. Se trata de ubicaciones de almacenamiento preferidas para las carpetas que contienen un tipo de objeto determinado. Un equivalente sería la carpeta Mis imágenes para los archivos de imagen de Windows. Si esta propiedad no existe, normalmente se usa [el \_ \_ nombre del objeto WPD](object-properties.md) .<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




