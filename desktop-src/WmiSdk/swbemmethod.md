---
description: Puede usar las propiedades del objeto SWbemMethod para inspeccionar una definición de método única de un objeto WMI. La llamada CreateObject de VBScript no puede crear este objeto.
ms.assetid: 461d5c41-4930-40cf-96e2-bc8cae335b60
ms.tgt_platform: multiple
title: Objeto SWbemMethod (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod
- ISWbemMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c750e81a3e41450e8cd32f37ccab6fee2f08439c6bc8fc8ae18bf0e4f106b551
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732665"
---
# <a name="swbemmethod-object"></a>Objeto SWbemMethod

Puede usar las propiedades del objeto **SWbemMethod** para inspeccionar una definición de método única de un objeto WMI. La llamada **CreateObject** de VBScript no puede crear este objeto.

Este objeto se puede usar para inspeccionar las definiciones de métodos. Para invocar los métodos, debe usar el acceso directo (vea [Manipular](manipulating-class-and-instance-information.md)información de clase e instancia ) en un objeto [**SWbemObject**](swbemobject.md) (que es el mecanismo recomendado) o la llamadaSWbemServices.Exe [**cMethod.**](swbemservices-execmethod.md)

> [!Note]  
> En esta versión de la API, no se admite el acceso de escritura a la información del método. Si desea definir métodos o modificar definiciones de método existentes, puede definir los cambios de método en un archivo MOF y enviar los cambios mediante el [compilador MOF](compiling-mof-files.md). Como alternativa, use la [API COM para WMI.](com-api-for-wmi.md)

 

## <a name="members"></a>Miembros

El **objeto SWbemMethod** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto SWbemMethod** tiene estas propiedades.



| Propiedad                                                      | Tipo de acceso          | Descripción                                                                                                                        |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**InParameters**](swbemmethod-inparameters.md)<br/>   | Solo lectura<br/> | Objeto [**SWbemObject**](swbemobject.md) cuyas propiedades definen los parámetros de entrada para este método.<br/>              |
| [**Nombre**](swbemmethod-name.md)<br/>                   | Solo lectura<br/> | Nombre del método.<br/>                                                                                                     |
| [**Origen**](swbemmethod-origin.md)<br/>               | Solo lectura<br/> | Clase de origen del método .<br/>                                                                                        |
| [**OutParameters**](swbemmethod-outparameters.md)<br/> | Solo lectura<br/> | Objeto [**SWbemObject**](swbemobject.md) cuyas propiedades definen los parámetros out y el tipo de valor devuelto de este método.<br/> |
| [**Calificadores\_**](swbemmethod-qualifiers-.md)<br/>    | Solo lectura<br/> | Objeto [**SWbemQualifierSet**](swbemqualifierset.md) que contiene los calificadores para este método.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethod<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemMethod<br/>                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de API de scripting](scripting-api-objects.md)
</dt> </dl>

 

 




