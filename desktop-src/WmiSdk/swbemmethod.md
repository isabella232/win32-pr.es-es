---
description: Puede utilizar las propiedades del objeto SWbemMethod para inspeccionar una definición de un solo método de un objeto WMI. Este objeto no se puede crear mediante la llamada CreateObject de VBScript.
ms.assetid: 461d5c41-4930-40cf-96e2-bc8cae335b60
ms.tgt_platform: multiple
title: Objeto SWbemMethod (Wbemdisp. h)
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
ms.openlocfilehash: 055957bf2774fc1e5c2e1f0149b00ece7b0a1bea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544675"
---
# <a name="swbemmethod-object"></a>Objeto SWbemMethod

Puede utilizar las propiedades del objeto **SWbemMethod** para inspeccionar una definición de un solo método de un objeto WMI. Este objeto no se puede crear mediante la llamada **CreateObject** de VBScript.

Este objeto se puede utilizar para inspeccionar las definiciones de los métodos. Para invocar los métodos, debe usar el acceso directo (vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md)) en un objeto [**SWbemObject**](swbemobject.md) (que es el mecanismo recomendado) o la llamada a [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) .

> [!Note]  
> En esta versión de la API, no se admite el acceso de escritura a la información del método. Si desea definir métodos o modificar las definiciones de método existentes, puede definir los cambios del método en un archivo MOF y enviar los cambios mediante el [compilador MOF](compiling-mof-files.md). También puede usar la [API com para WMI](com-api-for-wmi.md).

 

## <a name="members"></a>Miembros

El objeto **SWbemMethod** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **SWbemMethod** tiene estas propiedades.



| Propiedad                                                      | Tipo de acceso          | Descripción                                                                                                                        |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**Parameters**](swbemmethod-inparameters.md)<br/>   | Solo lectura<br/> | Objeto [**SWbemObject**](swbemobject.md) cuyas propiedades definen los parámetros de entrada para este método.<br/>              |
| [**Name**](swbemmethod-name.md)<br/>                   | Solo lectura<br/> | Nombre del método.<br/>                                                                                                     |
| [**Origen**](swbemmethod-origin.md)<br/>               | Solo lectura<br/> | Clase de origen del método.<br/>                                                                                        |
| [**Parameters**](swbemmethod-outparameters.md)<br/> | Solo lectura<br/> | Objeto [**SWbemObject**](swbemobject.md) cuyas propiedades definen los parámetros out y el tipo de valor devuelto de este método.<br/> |
| [**Calificadores\_**](swbemmethod-qualifiers-.md)<br/>    | Solo lectura<br/> | Un objeto [**SWbemQualifierSet**](swbemqualifierset.md) que contiene los calificadores de este método.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethod<br/>                                                           |
| IID<br/>                      | \_ISWBEMMETHOD IID<br/>                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Scripting de objetos de API](scripting-api-objects.md)
</dt> </dl>

 

 




