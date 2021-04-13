---
title: Constantes de enumeración (WSManDisp. h)
description: La enumeración contiene constantes, como se muestra en la lista siguiente, que se usa en el parámetro flags mediante llamadas a Session. Enumerate y IWSManSession Enumerate.
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
ms.openlocfilehash: e422f688fea992ee2d9b1d0d25af00a1d24ad798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422117"
---
# <a name="enumeration-constants"></a>Constantes de enumeración

La enumeración **\_ \_ WSManEnumFlags** contiene constantes, como se muestra en la lista siguiente, que se usa en el parámetro *Flags* mediante llamadas a [**Session. Enumerate**](session-enumerate.md) y [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

Tenga en cuenta que **WSManFlagReturnObject** y **WSManFlagHierarchyDeep** son el valor predeterminado si no se especifica el parámetro *Flags* .

<dl> <dt>

<span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**WSManFlagReturnObject**
</dt> <dd> <dl> <dt>

0 (0X0)
</dt> <dt>



Los lotes contienen las instancias XML solicitadas. Este es el valor predeterminado del parámetro de marca.

El método de scripting asociado es [**WSMan. EnumerationFlagReturnObject**](wsman-enumerationflagreturnobject.md) y el método de C++ es [**IWSManEx. EnumerationFlagReturnObject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject).


</dt> </dl> </dd> <dt>

<span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Esta marca controla cómo WinRM interpreta el parámetro de *filtro* en la llamada a [**Session. Enumerate**](session-enumerate.md) .

El formato del filtro puede ser un fragmento XML o una cadena de texto sin formato. El formato viene determinado por el [*dialecto de filtro*](windows-remote-management-glossary.md) del [*filtro*](windows-remote-management-glossary.md) usado en la llamada a [**Session. Enumerate**](session-enumerate.md) o [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate), que es específico de la operación realizada.

Si no se especifica el parámetro de *dialecto* , WinRM intenta determinar el dialecto en función del primer carácter del filtro. Si el primer carácter es <, pero el filtro no es realmente un fragmento XML, se debe establecer esta marca. Por ejemplo, un filtro en el formato siguiente requiere que establezca **WSManFlagNonXmlText** para que el filtro se interprete correctamente:

`<25 && > 1`

Si el filtro es un fragmento XML, esta marca no es necesaria porque el fragmento comienza con <, que WinRM interpreta correctamente como XML. Por ejemplo,

`<filter>select * from aDataStructure</filter>`

Si el filtro está en texto sin formato que no comienza con <, esta marca no es obligatoria. Por ejemplo,

`select * from aDataStructure`

El método de scripting asociado es [**WSMan. EnumerationFlagNonXmlText**](wsman-enumerationflagnonxmltext.md) y el método de C++ es [**IWSManEx. EnumerationFlagNonXmlText**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).


</dt> </dl> </dd> <dt>

<span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**
</dt> <dd> <dl> <dt>

2 (0X2)
</dt> <dt>



Los lotes contienen referencias de punto de conexión (EPRs) para las instancias XML correspondientes, pero no las instancias reales.

El método de scripting asociado es [**WSMan. EnumerationFlagReturnEPR**](wsman-enumerationflagreturnepr.md) y el método de C++ es [**IWSManEx. EnumerationFlagReturnEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).


</dt> </dl> </dd> <dt>

<span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Los lotes contienen las instancias XML solicitadas y las EPRs correspondientes contenidas en un elemento [*wsman: items*](windows-remote-management-glossary.md) .

El método de scripting asociado es [**WSMan. EnumerationFlagReturnObjectAndEPR**](wsman-enumerationflagreturnobjectandepr.md) y el método de C++ es [**IWSManEx. EnumerationFlagReturnObjectAndEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr).


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**
</dt> <dd> <dl> <dt>

0 (0X0)
</dt> <dt>



Las instancias de clase derivada se incluyen y se representan según sus esquemas reales.

El método de scripting asociado es [**WSMan. EnumerationFlagHierarchyDeep**](wsman-enumerationflaghierarchydeep.md) y el método de C++ es [**IWSManEx. EnumerationFlagHierarchyDeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Se excluyen las instancias de la clase derivada. Solo se muestran las instancias del tipo solicitado.

El método de scripting asociado es [**WSMan. EnumerationFlagHierarchyShallow**](wsman-enumerationflaghierarchyshallow.md) y el método de C++ es [**IWSManEx. EnumerationFlagHierarchyShallow**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow).


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Las instancias de clase derivada se incluyen y se representan según el esquema de la clase base. No se muestran las propiedades definidas en la clase derivada.

El método de scripting asociado es [**WSMan. EnumerationFlagHierarchyDeepBasePropsOnly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) y el método de C++ es [**IWSManEx. EnumerationFlagHierarchyDeepBasePropsOnly**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes y enumeraciones de WinRM](winrm-constants-and-enumerations.md)
</dt> <dt>

[Enumerar o enumerar todas las instancias de un recurso](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[Consultar instancias específicas de un recurso](querying-for-specific-instances-of-a-resource.md)
</dt> </dl>

 

 





