---
description: La propiedad Qualifiers \_ del objeto SWbemObject devuelve un objeto SWbemQualifierSet que es una colección de los calificadores de la clase o la instancia actual. Esta propiedad es de solo lectura.
ms.assetid: 5ecae751-0d83-4ad6-9840-ef47f76b1ff6
ms.tgt_platform: multiple
title: Propiedad SWbemObject.Qualifiers_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Qualifiers_
- ISWbemObject.Qualifiers_
- ISWbemObject.get_Qualifiers_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f9526596b7ae4a387cd0751ad95aff3b97dcc817
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715736"
---
# <a name="swbemobjectqualifiers_-property"></a>SWbemObject. Qualifiers \_ (propiedad)

La propiedad **Qualifiers \_** del objeto [**SWbemObject**](swbemobject.md) devuelve un objeto [**SWbemQualifierSet**](swbemqualifierset.md) que es una colección de los calificadores de la clase o la instancia actual. Esta propiedad es de solo lectura.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemObject.Qualifiers_ As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="examples"></a>Ejemplos

La [lista de todos los calificadores de un](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) ejemplo de código VBScript de clase WMI en la galería de TechNet usa la propiedad calificador \_ para enumerar los calificadores de clase de una clase WMI especificada.

En el ejemplo de código de [lista de todas las clases abstractas de WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript de la galería de TechNet se enumeran todas las clases abstractas de WMI definidas en el \\ espacio de nombres root cimv2.

En el ejemplo de código de [lista de todas las clases dinámicas en WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript se usa la \_ propiedad Qualifier para enumerar todas las clases dinámicas de WMI (incluidas las clases de asociación) definidas en el \\ espacio de nombres root cimv2.

En el ejemplo de código de PowerShell de [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) en la galería de TechNet se enumeran todas las propiedades que se escriben en el espacio de nombres especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | \_ISWBEMOBJECT IID<br/>                                                            |



 

 




