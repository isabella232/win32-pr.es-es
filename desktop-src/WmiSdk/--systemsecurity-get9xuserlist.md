---
description: Obtiene los derechos de acceso remoto para una lista de usuarios individuales en equipos que ejecutan versiones obsoletas de Windows , donde el control de acceso a través de Windows descriptores de seguridad no está disponible.
ms.assetid: 79a596db-5f85-4664-8989-f309286eca0d
ms.tgt_platform: multiple
title: __SystemSecurity::Get9XUserList (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Get9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: cfb6f0b9bb503e212e00d5343b55d6a9e20fbc8acfb0a5b534e8848cc6d3d931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110108"
---
# <a name="__systemsecurityget9xuserlist-method"></a>\_\_SystemSecurity::Get9XUserList (método)

El [**\_ \_ método SystemSecurity::Set9XUserList**](--systemsecurity-set9xuserlist.md) obtiene los derechos de acceso remoto para una lista de usuarios individuales en equipos que ejecutan versiones obsoletas de Windows , donde el control de acceso a través de Windows descriptores de seguridad no está disponible.

Esto funciona de forma similar al descriptor de seguridad, pero es más limitado. No se admiten grupos y no hay ningún control sobre el acceso local, porque el usuario local siempre tiene acceso completo. Se permiten las entradas de control de acceso de denegación y de permiso (ACE) y, debido a esto, el orden ace es importante en la lista de control de acceso discrecional (DACL). Para obtener más información, [vea Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)(Orden de A CA en una DACL).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Get9XUserList(
  [out] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ul* \[ out\]
</dt> <dd>

Matriz de usuarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **HRESULT** que indica el estado de la llamada al método. En la lista siguiente se enumeran los valores devueltos que son significativos **para Get9XUserList**. Para scripting y Visual Basic, el resultado puede ser [OutParameters.ReturnValue.](parsing-outparameters-objects.md) Para obtener más información, vea [Construir objetos InParameters y Analizar objetos OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**MÉTODO WBEM \_ E \_ \_ DESHABILITADO**
</dt> <dd>

Este método no se admite en las versiones admitidas de Windows.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[**\_\_SystemSecurity::GetSD**](--systemsecurity-getsd.md)
</dt> <dt>

[**\_\_SystemSecurity::SetSD**](--systemsecurity-setsd.md)
</dt> <dt>

[**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**SecurityDescriptor de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Protección de espacios de nombres WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Constantes de seguridad WMI](wmi-security-constants.md)
</dt> </dl>

 

