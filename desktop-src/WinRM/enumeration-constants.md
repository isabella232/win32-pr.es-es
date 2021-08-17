---
title: Constantes de enumeración (WSManDisp.h)
description: La enumeración contiene constantes, como se muestra en la lista siguiente, que las llamadas a Session.Enumerate e IWSManSession Enumerate usan en el parámetro flags.
ms.assetid: c0f2763b-a549-43d5-84a6-8cebf33a1ea2
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagReturnObject
- WSManFlagNonXmlText
- EnumerationFlagReturnEPR
- WSManFlagReturnObjectAndEPR
- WSManFlagHierarchyDeep
- WSManFlagHierarchyShallow
- WSManFlagHierarchyDeepBasePropsOnly
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c8182352d2ebf3763a38f74dd6f100dc836e88cfa10212ffaa971048ebd1aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113267"
---
# <a name="enumeration-constants"></a>Constantes de enumeración

La enumeración **\_ \_ WSManEnumFlags** contiene constantes, como se muestra en la lista siguiente, que las llamadas a [**Session.Enumerate**](session-enumerate.md) e [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)usan en el parámetro *flags.*

Tenga en cuenta **que WSManFlagReturnObject** y **WSManFlagHierarchyDeep** son el valor predeterminado si no se especifica el parámetro *flags.*

<dl> <dt>

<span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**WSManFlagReturnObject**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Los lotes contienen las instancias XML solicitadas. Este es el valor predeterminado para el parámetro flag.

El método de scripting asociado es [**WSMan.EnumerationFlagReturnObject**](wsman-enumerationflagreturnobject.md) y el método de C++ [**es IWSManEx.EnumerationFlagReturnObject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject).


</dt> </dl> </dd> <dt>

<span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Esta marca controla cómo *WinRM* interpreta el parámetro de filtro en la llamada a [**Session.Enumerate.**](session-enumerate.md)

El formato del filtro puede ser un fragmento XML o una cadena de texto sin formato. El formato viene determinado por [](windows-remote-management-glossary.md) el [*dialecto*](windows-remote-management-glossary.md) de filtro del filtro utilizado en la llamada a [**Session.Enumerate**](session-enumerate.md) o [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate), que es específico de la operación realizada.

Si no *se especifica* el parámetro dialecto, WinRM intenta determinar el dialecto en función del primer carácter del filtro. Si el primer carácter es <, pero el filtro no es realmente un fragmento XML, se debe establecer esta marca. Por ejemplo, un filtro con el formato siguiente requiere que establezca **WSManFlagNonXmlText** para que el filtro se interprete correctamente:

`<25 && > 1`

Si el filtro es un fragmento XML, esta marca no es necesaria porque el fragmento comienza por <, que WinRM interpreta correctamente como XML. Por ejemplo,

`<filter>select * from aDataStructure</filter>`

Si el filtro está en texto sin formato que no comienza con <, esta marca no es necesaria. Por ejemplo,

`select * from aDataStructure`

El método de scripting asociado es [**WSMan.EnumerationFlagNonXmlText**](wsman-enumerationflagnonxmltext.md) y el método de C++ [**es IWSManEx.EnumerationFlagNonXmlText.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext)


</dt> </dl> </dd> <dt>

<span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Los lotes contienen referencias de punto de conexión (EPR) para las instancias XML correspondientes, pero no las instancias reales.

El método de scripting asociado es [**WSMan.EnumerationFlagReturnEPR**](wsman-enumerationflagreturnepr.md) y el método de C++ [**es IWSManEx.EnumerationFlagReturnEPR.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr)


</dt> </dl> </dd> <dt>

<span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Los lotes contienen las instancias XML solicitadas y las EPR correspondientes contenidas en un [*elemento wsman:Items.*](windows-remote-management-glossary.md)

El método de scripting asociado es [**WSMan.EnumerationFlagReturnObjectAndEPR**](wsman-enumerationflagreturnobjectandepr.md) y el método de C++ [**es IWSManEx.EnumerationFlagReturnObjectAndEPR.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr)


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Las instancias de clase derivadas se incluyen y se representan según sus esquemas reales.

El método de scripting asociado es [**WSMan.EnumerationFlagHierarchyDeep**](wsman-enumerationflaghierarchydeep.md) y el método de C++ [**es IWSManEx.EnumerationFlagHierarchyDeep.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep)


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Se excluyen las instancias de clase derivada. Solo se muestran las instancias del tipo solicitado.

El método de scripting asociado es [**WSMan.EnumerationFlagHierarchyShallow**](wsman-enumerationflaghierarchyshallow.md) y el método de C++ [**es IWSManEx.EnumerationFlagHierarchyShallow.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow)


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Las instancias de clase derivadas se incluyen y se representan según el esquema de clase base. No se muestran las propiedades definidas en la clase derivada.

El método de scripting asociado es [**WSMan.EnumerationFlagHierarchyDeepBasePropsOnly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) y el método de C++ [**es IWSManEx.EnumerationFlagHierarchyDeepBasePropsOnly.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly)


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes y enumeraciones de WinRM](winrm-constants-and-enumerations.md)
</dt> <dt>

[Enumerar o enumerar todas las instancias de un recurso](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[Consulta de instancias específicas de un recurso](querying-for-specific-instances-of-a-resource.md)
</dt> </dl>

 

 





