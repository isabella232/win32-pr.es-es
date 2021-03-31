---
description: Extiende la funcionalidad de SWbemServices.
ms.assetid: def514a9-eca4-41de-87cd-c9f964a71f68
ms.tgt_platform: multiple
title: Objeto SWbemServicesEx (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx
- ISWbemServicesEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8ed41cbab38e24958705c24aefc9ea5e9e67357e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155817"
---
# <a name="swbemservicesex-object"></a>Objeto SWbemServicesEx

El objeto **SWbemServicesEx** amplía la funcionalidad de [**SWbemServices**](swbemservices.md). Los métodos [**Put**](swbemservicesex-put.md) y [**PutAsync**](swbemservicesex-putasync.md) permiten guardar una clase o una instancia en varios espacios de nombres o en un espacio de nombres diferente del que se creó en una instancia. Este objeto no se puede crear mediante la llamada [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) de VBScript.

## <a name="members"></a>Miembros

El objeto **SWbemServicesEx** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El objeto **SWbemServicesEx** tiene estos métodos.



| Método                                       | Descripción                                                                                                                                                                                                               |
|:---------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Pondrán**](swbemservicesex-put.md)           | Guarda el objeto en el espacio de nombres enlazado al objeto **SWbemServicesEx** y devuelve un objeto [**SWbemObjectPath**](swbemobjectpath.md) que contiene la ruta de acceso del objeto en el que se escribieron los datos.<br/> |
| [**PutAsync**](swbemservicesex-putasync.md) | Guarda un objeto de forma asincrónica en un espacio de nombres.<br/>                                                                                                                                                                 |



 

## <a name="remarks"></a>Observaciones

Se puede llamar a los métodos de esta clase en el modo semisincrónico o en el modo asincrónico. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ ISWbemServicesEx<br/>                                                      |
| IID<br/>                      | \_ISWBEMSERVICESEX IID<br/>                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Scripting de objetos de API](scripting-api-objects.md)
</dt> <dt>

[Llamar a un método](calling-a-method.md)
</dt> </dl>

 

