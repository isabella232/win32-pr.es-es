---
description: Establece los derechos de acceso remoto para una lista de usuarios individuales en equipos que ejecutan versiones obsoletas de Windows, donde el control de acceso a través de Windows descriptores de seguridad no está disponible.
ms.assetid: f6da65d3-86dd-4fc8-b4c0-f7ddc8536d4e
ms.tgt_platform: multiple
title: __SystemSecurity::Set9XUserList (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Set9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: d1185fa91d9d12e240f592d458b975b650947cf5b8cd1b289a7e016b455556a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118109966"
---
# <a name="__systemsecurityset9xuserlist-method"></a>\_\_SystemSecurity::Set9XUserList (método)

El **\_ \_ método SystemSecurity::Set9XUserList** establece los derechos de acceso remoto para una lista de usuarios individuales en equipos que ejecutan versiones obsoletas de Windows, donde el control de acceso a través de descriptores de seguridad de Windows no está disponible.

La lista se especifica como una matriz de objetos incrustados donde cada objeto es una instancia de la [**\_ \_ clase NTLMUser9X.**](--ntlmuser9x.md) Esto funciona de forma similar al descriptor de seguridad, pero es más limitado. No se admiten grupos y no hay ningún control sobre el acceso local, porque el usuario local siempre tiene acceso completo. Se permiten las entradas de control de acceso de denegación y de permiso (ACE) y, debido a esto, el orden ace es importante en la lista de control de acceso discrecional (DACL). Para obtener más información, [vea Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)(Orden de A CA en una DACL).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Set9XUserList(
  [in] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ul* \[ En\]
</dt> <dd>

Matriz de usuarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **HRESULT** que indica el estado de la llamada al método. En la lista siguiente se enumeran los valores devueltos que son significativos **para Set9XUserList**. Para el scripting Visual Basic aplicaciones, el resultado se puede obtener de [OutParameters.ReturnValue](parsing-outparameters-objects.md). Para obtener más información, vea [Construir objetos InParameters y Analizar objetos OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**MÉTODO WBEM \_ E \_ \_ DESHABILITADO**
</dt> <dd>

No se admite este método.

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

 

