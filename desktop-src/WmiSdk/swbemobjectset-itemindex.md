---
description: Devuelve el SWbemObject asociado al índice especificado en la colección.
ms.assetid: 75830f78-0489-4fae-bf9c-2eee8526232e
ms.tgt_platform: multiple
title: Método SWbemObjectSet. ItemIndex (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 606a09ebf54f0a31dbe14e10abd52a7e92d815d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706979"
---
# <a name="swbemobjectsetitemindex-method"></a>SWbemObjectSet. ItemIndex (método)

El método **itemIndex** devuelve el [**SWbemObject**](swbemobject.md) asociado con el índice especificado en la colección. El índice indica la posición del elemento dentro de la colección. La numeración de la colección comienza en cero.

## <a name="syntax"></a>Sintaxis


```VB
objWbemObject = .ItemIndex( _
  ByVal lIndex _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lIndex* 
</dt> <dd>

Índice del elemento de la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, el objeto [**SWbemObject**](swbemobject.md) solicitado devuelve.

## <a name="error-codes"></a>Códigos de error

Una vez finalizado el método [**Item**](swbemobjectset-item.md) , el objeto **Err** puede contener uno de los códigos de error siguientes.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Se especificó un parámetro no válido. Se devuelve este error si se proporciona un número de índice negativo.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insuficiente para completar la operación.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

No se encontró el elemento solicitado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El método **itemIndex** permite que los scripts y las aplicaciones de los clientes WMI escritos en cualquier lenguaje sean una manera uniforme de manipular una colección como una matriz. Este método se puede usar con colecciones [**SWbemObjectSet**](swbemobjectset.md) . Las consultas, como [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md), [**SWbemServices. References**](swbemservices-referencesto.md), [**SWbemServices. instances**](swbemservices-instancesof.md)o [**SWbemServices.ExecQuery**](swbemservices-execquery.md) devuelven colecciones de **SWbemObjectSet** . El método **itemIndex** no funciona con colecciones que no contienen [**SWbemObjects**](swbemobject.md), como [**SWbemMethodSet**](swbemmethodset.md), [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md), [**SWbemPropertySet**](swbempropertyset.md)y [**SWbemQualifierSet**](swbemqualifierset.md).

**ItemIndex** también se puede utilizar para obtener la instancia única de una clase singleton.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se consulta una colección de todas las instancias de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) y, a continuación, se muestran los nombres de los tres primeros procesos.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colProcesses = _
    objWMIService.Execquery("Select * from Win32_Process")
Wscript.Echo  colProcesses.ItemIndex(0).Name
Wscript.Echo  colProcesses.ItemIndex(1).Name
Wscript.Echo  colProcesses.ItemIndex(2).Name
```



Solo existe una instancia de [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) para cada instalación de sistema operativo. La creación de la ruta de acceso [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) para obtener la instancia única es difícil, por lo que los scripts suelen enumerar **Win32 \_ OperatingSystem** aunque solo haya una instancia disponible. En el ejemplo de código de VBScript siguiente se muestra cómo utilizar el método **itemIndex** para llegar a un sistema **\_ operativo de Win32** sin usar un bucle **for each** .


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery _
    ("Select * from Win32_OperatingSystem")

Wscript.Echo "Caption: " & colOperatingSystems.ItemIndex(0).Caption
```



El siguiente ejemplo de código de VBScript obtiene instancias asociadas con el [**\_ OperatingSystem de Win32**](/windows/desktop/CIMWin32Prov/win32-operatingsystem), como [**\_ SystemOperatingSystem de Win32**](/windows/desktop/CIMWin32Prov/win32-systemoperatingsystem).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colOS = _
    objWMIService.Execquery("Select * from Win32_OperatingSystem")
    Wscript.Echo  colOS.ItemIndex(0).Name

set colAssociators = colOS.ItemIndex(0).Associators_
    For Each Associator in colAssociators 
        Wscript.Echo Associator.Path_.RelPath  
    Next
```



La siguiente salida de ejemplo de código muestra las instancias asociadas a [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).

``` syntax
Windows Server 2008 
    |C:\Windows|\Device\Harddisk0\Partition1
Win32_ComputerSystem.Name="Test1"
Win32_AutochkSetting.SettingID="Windows Server 2008 
    |C:\\Windows|\\Device\\Harddisk0\\Partition1"
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectSet<br/>                                                        |
| IID<br/>                      | \_ISWBEMOBJECTSET IID<br/>                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemObjectSet**](swbemobjectset.md)
</dt> </dl>

 

