---
description: Un objeto SWbemMethodSet es una colección de objetos SWbemMethod. Los elementos se recuperan mediante el método Item. Para obtener más información, vea obtener acceso a una colección. Este objeto no se puede crear mediante la llamada CreateObject de VBScript.
ms.assetid: 0ca2601f-ed40-472e-b4f2-eee750c8c8d1
ms.tgt_platform: multiple
title: Objeto SWbemMethodSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet
- ISWbemMethodSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d47c4dc8335077d6f8568be4b56200558942ac39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910281"
---
# <a name="swbemmethodset-object"></a>Objeto SWbemMethodSet

Un objeto **SWbemMethodSet** es una colección de objetos [**SWbemMethod**](swbemmethod.md) . Los elementos se recuperan mediante el método [**Item**](swbemmethodset-item.md) . Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md). Este objeto no se puede crear mediante la llamada **CreateObject** de VBScript.

> [!Note]  
> En esta versión de la API, no se admite el acceso de escritura a la información del método. Si desea definir métodos o modificar las definiciones de método existentes, puede definir los cambios del método en un archivo MOF y enviar los cambios mediante el compilador MOF. También puede usar la API COM de WMI.

 

## <a name="members"></a>Miembros

El objeto **SWbemMethodSet** tiene estos tipos de miembros:

-   [Métodos](#swbemmethodset-object)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **SWbemMethodSet** tiene estos métodos.



| Método                              | Descripción                                                                                                                                  |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Elemento**](swbemmethodset-item.md) | Recupera un objeto [**SWbemMethod**](swbemmethod.md) de la colección. Este es el método de automatización predeterminado de este objeto.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **SWbemMethodSet** tiene estas propiedades.



| Propiedad                                         | Tipo de acceso          | Descripción                                       |
|:-------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**Contabiliza**](swbemmethodset-count.md)<br/> | Solo lectura<br/> | Número de elementos de la colección.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethodSet<br/>                                                        |
| IID<br/>                      | \_ISWBEMMETHODSET IID<br/>                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Scripting de objetos de API](scripting-api-objects.md)
</dt> </dl>

 

 




