---
title: Tipos de modificación de atributos ADSI (iAds. h)
description: Se usa con el miembro dwControlCode de la estructura de información de atributos de ADS \_ \_ para especificar el tipo de operación que se va a realizar cuando se modifica un atributo con el método SetObjectAttributes de IDirectoryObject.
ms.assetid: e9a454c8-e067-4730-97f4-85c4f5889e05
ms.tgt_platform: multiple
keywords:
- tipos de modificación de atributos ADSI
topic_type:
- apiref
api_name:
- ADS_ATTR_CLEAR
- ADS_ATTR_UPDATE
- ADS_ATTR_APPEND
- ADS_ATTR_DELETE
api_location:
- Iads.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a739241fd52a7d45d58a1b36bb7de838234d6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079084"
---
# <a name="adsi-attribute-modification-types"></a>Tipos de modificación de atributos ADSI

Las constantes siguientes se usan con el miembro **dwControlCode** de la estructura [**ADS \_ ATTR \_ info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) para especificar el tipo de operación que se va a realizar cuando se modifica un atributo con el método [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) . Para obtener más información sobre el uso de estos valores, vea [modificar atributos con ADSI](modifying-attributes-with-adsi.md).

<dl> <dt>

<span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**\_claridad del atributo ADS \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Hace que se quiten todos los valores de atributo de un objeto.


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**\_actualización de atributos de ADS \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Hace que se actualicen los valores de atributo especificados.


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**ADS \_ ATTR \_ Append**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Hace que los valores de atributo especificados se anexen a los valores de atributo existentes.


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**ADS \_ ATTR \_ eliminar**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Hace que los valores de atributo especificados se quiten de un objeto.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Estas constantes están diseñadas para usarse con la estructura [**de \_ \_ información de atributos de ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) en el método [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) . Estas constantes no se deben confundir con miembros de la enumeración de la enumeración de la [**\_ operación de propiedad \_ \_ ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) , que están diseñadas para usarse con el método [**IADs::P Utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                    |
| Encabezado<br/>                   | <dl> <dt>IAds. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_información de atributos de ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)
</dt> <dt>

[**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)
</dt> <dt>

[Modificar atributos con ADSI](modifying-attributes-with-adsi.md)
</dt> </dl>

 

 





