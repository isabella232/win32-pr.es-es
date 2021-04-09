---
title: Métodos de la propiedad IADsComputer (iAds. h)
description: Los métodos de la interfaz IADsComputer leen y escriben las propiedades descritas en este tema. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: c990b6bb-6256-4216-9435-c85c67db4d13
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsComputer ADSI
topic_type:
- apiref
api_name:
- IADsComputer Property Methods
- IADsComputer.ComputerID
- IADsComputer.get_ComputerID
- IADsComputer.Department
- IADsComputer.get_Department
- IADsComputer.put_Department
- IADsComputer.Description
- IADsComputer.get_Description
- IADsComputer.put_Description
- IADsComputer.Division
- IADsComputer.get_Division
- IADsComputer.put_Division
- IADsComputer.Location
- IADsComputer.get_Location
- IADsComputer.put_Location
- IADsComputer.MemorySize
- IADsComputer.get_MemorySize
- IADsComputer.put_MemorySize
- IADsComputer.Model
- IADsComputer.get_Model
- IADsComputer.put_Model
- IADsComputer.NetAddresses
- IADsComputer.get_NetAddresses
- IADsComputer.put_NetAddresses
- IADsComputer.OperatingSystem
- IADsComputer.get_OperatingSystem
- IADsComputer.put_OperatingSystem
- IADsComputer.OperatingSystemVersion
- IADsComputer.get_OperatingSystemVersion
- IADsComputer.put_OperatingSystemVersion
- IADsComputer.Owner
- IADsComputer.get_Owner
- IADsComputer.put_Owner
- IADsComputer.PrimaryUser
- IADsComputer.get_PrimaryUser
- IADsComputer.put_PrimaryUser
- IADsComputer.Processor
- IADsComputer.get_Processor
- IADsComputer.put_Processor
- IADsComputer.ProcessorCount
- IADsComputer.get_ProcessorCount
- IADsComputer.put_ProcessorCount
- IADsComputer.Role
- IADsComputer.get_Role
- IADsComputer.put_Role
- IADsComputer.Site
- IADsComputer.get_Site
- IADsComputer.StorageCapacity
- IADsComputer.get_StorageCapacity
- IADsComputer.put_StorageCapacity
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2f3c455e2e43436627b62d142781bb6a605bef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905466"
---
# <a name="iadscomputer-property-methods"></a>Métodos de propiedad IADsComputer

Los métodos de la interfaz [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) leen y escriben las propiedades descritas en este tema. Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**ComputerID**
</dt> <dd> <dl>

Identificador único global asignado a cada equipo.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerID(
  [out] BSTR* pbstrComputerID
);
```


</dt> </dl> </dd> <dt>

**Departamento**
</dt> <dd> <dl>

Unidad organizativa (OU), como Departamento, a la que pertenece este equipo.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Department(
  [out] BSTR* pbstrDepartment
);
HRESULT put_Department(
  [in] BSTR bstrDepartment
);
```


</dt> </dl> </dd> <dt>

**Descripción**
</dt> <dd> <dl>

La descripción de este equipo.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

**División**
</dt> <dd> <dl>

La división, dentro de una organización, a la que pertenece este equipo.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Division(
  [out] BSTR* pbstrDivision
);
HRESULT put_Division(
  [in] BSTR bstrDivision
);
```


</dt> </dl> </dd> <dt>

**Ubicación**
</dt> <dd> <dl>

Ubicación física asignada de este equipo.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Location(
  [out] BSTR* pbstrLocation
);
HRESULT put_Location(
  [in] BSTR bstrLocation
);
```


</dt> </dl> </dd> <dt>

**MemorySize**
</dt> <dd> <dl>

Tamaño, en megabytes, de la memoria de acceso aleatorio para este equipo.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MemorySize(
  [out] BSTR* pbstrMemorySize
);
HRESULT put_MemorySize(
  [in] BSTR bstrMemorySize
);
```


</dt> </dl> </dd> <dt>

**Modelo**
</dt> <dd> <dl>

Marca y modelo de este equipo.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Model(
  [out] BSTR* pbstrModel
);
HRESULT put_Model(
  [in] BSTR bstrModel
);
```


</dt> </dl> </dd> <dt>

**NetAddresses**
</dt> <dd> <dl>

Una matriz de campos NetAddress que representan las direcciones a las que se puede tener acceso a este equipo. NetAddress es un **BSTR** específico del proveedor que se compone de dos subcadenas separadas por dos puntos (:). La subcadena izquierda indica el tipo de dirección y la subcadena derecha es una representación de cadena de una dirección de ese tipo. Por ejemplo, las direcciones TCP/IP tienen el siguiente formato: IP: 100.201.301.45. Las direcciones de tipo IPX tienen el formato: IPX: 10.123456.80.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NetAddresses(
  [out] VARIANT* pvNetAddresses
);
HRESULT put_NetAddresses(
  [in] VARIANT vNetAddresses
);
```


</dt> </dl> </dd> <dt>

**Identifica**
</dt> <dd> <dl>

Sistema operativo que se usa en este equipo.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OperatingSystem(
  [out] BSTR* pbstrOperatingSystem
);
HRESULT put_OperatingSystem(
  [in] BSTR bstrOperatingSystem
);
```


</dt> </dl> </dd> <dt>

**OperatingSystemVersion**
</dt> <dd> <dl>

La versión del sistema operativo que se usa en este equipo.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OperatingSystemVersion(
  [out] BSTR* pbstrOperatingSystemVersion
);
HRESULT put_OperatingSystemVersion(
  [in] BSTR bstrOperatingSystemVersion
);
```


</dt> </dl> </dd> <dt>

**Propietario**
</dt> <dd> <dl>

La persona a la que se asigna este equipo. Esta persona también debe tener una licencia para ejecutar el software instalado.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Owner(
  [out] BSTR* pbstrOwner
);
HRESULT put_Owner(
  [in] BSTR bstrOwner
);
```


</dt> </dl> </dd> <dt>

**PrimaryUser**
</dt> <dd> <dl>

El nombre de la persona de contacto, como un administrador, para este equipo.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryUser(
  [out] BSTR* pbstrPrimaryUser
);
HRESULT put_PrimaryUser(
  [in] BSTR bstrPrimaryUser
);
```


</dt> </dl> </dd> <dt>

**Procesador**
</dt> <dd> <dl>

Tipo de procesador.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Processor(
  [out] BSTR* pbstrProcessor
);
HRESULT put_Processor(
  [in] BSTR bstrProcessor
);
```


</dt> </dl> </dd> <dt>

**ProcessorCount**
</dt> <dd> <dl>

El número de procesadores instalados.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ProcessorCount(
  [out] BSTR* pbstrProcessorCount
);
HRESULT put_ProcessorCount(
  [in] BSTR bstrProcessorCount
);
```


</dt> </dl> </dd> <dt>

**Rol**
</dt> <dd> <dl>

El rol de este equipo, por ejemplo, estación de trabajo, servidor o controlador de dominio.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Role(
  [out] BSTR* pbstrRole
);
HRESULT put_Role(
  [in] BSTR bstrRole
);
```


</dt> </dl> </dd> <dt>

**Sitio**
</dt> <dd> <dl>

Identificador único global que identifica el sitio en el que se instaló este equipo. Un sitio es una región física de buena conectividad en una red.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Site(
  [out] BSTR* pbstrSite
);
```


</dt> </dl> </dd> <dt>

**StorageCapacity**
</dt> <dd> <dl>

Tamaño, en megabytes, del disco.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StorageCapacity(
  [out] BSTR* pbstrStorageCapacity
);
HRESULT put_StorageCapacity(
  [in] BSTR bstrStorageCapacity
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Observaciones

Distintos proveedores pueden optar por exponer distintas propiedades de un objeto de equipo. Para obtener más información, consulte [ADSI System Providers](adsi-system-providers.md).

Puede descubrir las propiedades que se admiten mediante la inspección de las propiedades obligatorias y opcionales a través de su clase de esquema. Para obtener más información, consulte la interfaz [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) .

Para examinar el estado de un equipo o para realizar la operación de apagado a través de la red, debe usar la interfaz [**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) .

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código Visual Basic se examinan las propiedades del equipo admitidas por el proveedor WinNT de ADSI.


```VB
Dim obj As IADs
On Error Resume Next

Set obj = GetObject("WinNT://myMachine,computer")
If (obj.Class = "Computer") Then
    MsgBox "Computer owner: " & obj.owner
    MsgBox "Computer division: " & obj.Division
    MsgBox "Computer operatingSystem: " & obj.OperatingSystem
    MsgBox "Computer operating System Version: " & obj.OperatingSystemVersion
    MsgBox "Computer processor: " & obj.Processor
    MsgBox "Computer processor Count: " & obj.ProcessorCount
End If
```



En el siguiente ejemplo de código de C++ se examinan las propiedades del equipo admitidas por el proveedor WinNT de ADSI.


```C++
IADsComputer *pComp = NULL;
LPWSTR adspath = L"WinNT://jeffsmith1,computer";
HRESULT hr = S_OK;
BSTR bstr = NULL;

hr = ADsGetObject(adspath,IID_IADsComputer,(void**)&pComp);
if(FAILED(hr)) {goto Cleanup;}

hr = pComp->get_Owner(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Computer owner: %S\n",bstr);
SysFreeString(bstr);

hr = pComp->get_OperatingSystem(&bstr);
if(FAILED(hr)) {goto Cleanup;}
printf("Operating System: %S\n",bstr);
SysFreeString(bstr);

Cleanup:
    if(pComp) pComp->Release();
    if(bstr) SysFreeString(bstr);
    return hr;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsComputer se define como EFE3CC70-1D9F-11cf-B1F3-02608C9E7553<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)
</dt> <dt>

[Proveedores de sistema ADSI](adsi-system-providers.md)
</dt> <dt>

[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)
</dt> <dt>

[Métodos de propiedad de interfaz](interface-property-methods.md)
</dt> </dl>

 

 





