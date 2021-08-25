---
description: El objeto SWbemProperty representa una única propiedad WMI de un objeto administrado. La llamada CreateObject de VBScript no puede crear este objeto.
ms.assetid: 2ddcfffa-a7b4-4fd6-926d-411de27f6212
ms.tgt_platform: multiple
title: Objeto SWbemProperty (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty
- ISWbemProperty
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 51f4b1b22849fc5a6ae22f49c5c30411563efb9d133cf2440c301eabfde18e0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898075"
---
# <a name="swbemproperty-object"></a>Objeto SWbemProperty

El **objeto SWbemProperty** representa una única propiedad WMI de un objeto administrado. La llamada [CreateObject](creating-an-object-using-vbscript.md) de VBScript no puede crear este objeto.

## <a name="members"></a>Miembros

El **objeto SWbemProperty** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto SWbemProperty** tiene estas propiedades.



| Propiedad                                                     | Tipo de acceso           | Descripción                                                                                                                   |
|:-------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**CIMType**](swbemproperty-cimtype.md)<br/>          | Solo lectura<br/>  | Tipo de esta propiedad.<br/>                                                                                             |
| [**IsArray**](swbemproperty-isarray.md)<br/>          | Solo lectura<br/>  | Valor booleano que indica si esta propiedad tiene un tipo de matriz.<br/>                                                   |
| [**IsLocal**](swbemproperty-islocal.md)<br/>          | Solo lectura<br/>  | Valor booleano que indica si esta propiedad es local.<br/>                                                            |
| [**Nombre**](swbemproperty-name.md)<br/>                | Solo lectura<br/>  | Nombre de esta propiedad WMI.<br/>                                                                                         |
| [**Origen**](swbemproperty-origin.md)<br/>            | Solo lectura<br/>  | Contiene la clase de origen de esta propiedad.<br/>                                                                   |
| [**Calificadores\_**](swbemproperty-qualifiers-.md)<br/> | Solo lectura<br/>  | Objeto [**SWbemQualifierSet,**](swbemqualifierset.md) que es la colección de calificadores para esta propiedad.<br/> |
| [**Value**](swbemproperty-value.md)<br/>              | Lectura/escritura<br/> | Valor real de esta propiedad. Esta es la propiedad de automatización predeterminada de este objeto .<br/>                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemProperty<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemProperty<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de API de scripting](scripting-api-objects.md)
</dt> </dl>

 

 




