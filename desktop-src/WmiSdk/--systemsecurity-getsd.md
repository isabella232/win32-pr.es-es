---
description: Obtiene el descriptor de seguridad para el espacio de nombres al que está conectado el usuario. Este método devuelve un descriptor de seguridad en formato binario de matriz de bytes. Si está escribiendo un script, use el método GetSecurityDescriptor.
ms.assetid: aeac1e7b-fcb8-4880-afd1-4950da37602b
ms.tgt_platform: multiple
title: Obtiene el método de la clase __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: d471db22a9f15a38ab693ae72332e5e1893b5c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706471"
---
# <a name="getsd-method-of-the-__systemsecurity-class"></a>Método obtiene de la \_ \_ clase SystemSecurity

El método que se **obtiene** obtiene el descriptor de seguridad para el espacio de nombres al que está conectado el usuario. Este método devuelve un descriptor de seguridad en formato binario de matriz de bytes. Si está escribiendo un script, use el método [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) . Para obtener más información, vea [proteger los espacios de nombres WMI](securing-wmi-namespaces.md) y [cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).

El usuario debe tener el permiso de **\_ control de lectura** . De forma predeterminada, los administradores tienen ese permiso. La única parte del descriptor de seguridad que se usa realmente es la lista de control de acceso discrecional (DACL). DACL puede contener ACE heredadas y no heredadas. Se permiten las ACE deny y allow.

Si está programando en C++, puede manipular el descriptor de seguridad binario mediante [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)y los métodos de conversión [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) y [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

## <a name="syntax"></a>Sintaxis


```mof
HRESULT GetSD(
  [out] uint8 SD[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SD* \[ enuncia\]
</dt> <dd>

Descriptor de seguridad en formato binario de matriz de bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor HRESULT** que indica el estado de la llamada al método. En la lista siguiente se enumeran los valores devueltos que son de importancia para se **obtiene**. En el caso de las aplicaciones de scripting y Visual Basic, el resultado se puede obtener de [Parameters. ReturnValue](parsing-outparameters-objects.md). Para obtener más información, consulte [construir objetos Parameters y analizar objetos Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**S \_ correcto**
</dt> <dd>

El método se ejecutó correctamente.

</dd> <dt>

**WBEM \_ E \_ acceso \_ denegado**
</dt> <dd>

El autor de la llamada no tiene derechos suficientes para llamar a este método.

</dd> <dt>

**WBEM \_ E \_ método \_ deshabilitado**
</dt> <dd>

Se intentó ejecutar este método en un sistema no compatible.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para obtener más información sobre cómo modificar la seguridad de los espacios de nombres mediante programación o manualmente, consulte protección de los [espacios de nombres WMI](securing-wmi-namespaces.md).

## <a name="examples"></a>Ejemplos

En el siguiente script se muestra cómo usar se **obtiene** para obtener el descriptor de seguridad actual del \\ espacio de nombres root Cimv2 y cambiarlo a la matriz de bytes que se muestra en **disjugada**.


```VB
Set objServices = GetObject("winmgmts:root\cimv2")
Set CimV2 = objServices.Get("__SystemSecurity=@")
ReturnValue = Cimv2.GetSD(arrSD)

If Err <> 0 Then
   WScript.Echo "Method returned error " & ReturnValue
End If

DisplaySD = "SD = {"
For I = Lbound(arrSD) To Ubound(arrSD)

   DisplaySD = DisplaySD & arrSD(I)

   If I <> Ubound(arrSD) Then
      DisplaySD = DisplaySD & ","
   End If

Next

DisplaySD = DisplaySD & "}"

WScript.Echo DisplaySD
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[Constantes de seguridad de WMI](wmi-security-constants.md)
</dt> <dt>

[**ACE de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**\_\_SystemSecurity:: establecido**](--systemsecurity-setsd.md)
</dt> <dt>

[**Descriptor de seguridad \_**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[**SecurityDescriptor de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Proteger los espacios de nombres de WMI](securing-wmi-namespaces.md)
</dt> </dl>

 

