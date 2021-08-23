---
description: La propiedad Qualifiers del objeto SWbemObject devuelve un objeto SWbemQualifierSet que es una colección de los calificadores para la clase o instancia \_ actual. Esta propiedad es de solo lectura.
ms.assetid: 5ecae751-0d83-4ad6-9840-ef47f76b1ff6
ms.tgt_platform: multiple
title: SWbemObject.Qualifiers_ propiedad (Wbemdisp.h)
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
ms.openlocfilehash: 3096b11399336a7dfcd9a36a314f6e569e24b29e8d27718345adbb55a9af0107
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732495"
---
# <a name="swbemobjectqualifiers_-property"></a>SWbemObject.Qualifiers, propiedad \_

La **propiedad \_ Qualifiers** del objeto [**SWbemObject**](swbemobject.md) devuelve un objeto [**SWbemQualifierSet**](swbemqualifierset.md) que es una colección de los calificadores para la clase o instancia actual. Esta propiedad es de solo lectura.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemObject.Qualifiers_ As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="examples"></a>Ejemplos

El ejemplo de código [List All the Qualifiers for a WMI Class](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) VBScript (Enumerar todos los calificadores de una clase WMI) de la Galería de TechNet usa la propiedad Qualifier para enumerar los calificadores de clase de una clase WMI \_ especificada.

En el ejemplo de código List [All Abstract Classes in WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript de la Galería de TechNet se enumeran todas las clases abstractas wmi definidas en el espacio de nombres raíz \\ cimv2.

El ejemplo de código [Enumerar](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) todas las clases dinámicas de WMI VBScript usa la propiedad Calificador para enumerar todas las clases dinámicas wmi (incluidas las clases de asociación) definidas en el espacio de nombres \_ raíz \\ cimv2.

El [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) de código de PowerShell en la Galería de TechNet muestra todas las propiedades que se pueden escribir en el espacio de nombres especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




