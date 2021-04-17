---
description: Establece los derechos de acceso remoto para una lista de usuarios individuales en equipos que ejecutan versiones obsoletas de Windows, donde el control de acceso a través de los descriptores de seguridad de Windows no está disponible.
ms.assetid: f6da65d3-86dd-4fc8-b4c0-f7ddc8536d4e
ms.tgt_platform: multiple
title: '__SystemSecurity:: Set9XUserList (método)'
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
ms.openlocfilehash: dd377da3adf55aef6a78576e1c978196f349f619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697597"
---
# <a name="__systemsecurityset9xuserlist-method"></a>\_\_SystemSecurity:: Set9XUserList (método)

El método **\_ \_ SystemSecurity:: Set9XUserList** establece los derechos de acceso remoto para una lista de usuarios individuales en equipos que ejecutan versiones obsoletas de Windows, donde el control de acceso a través de los descriptores de seguridad de Windows no está disponible.

La lista se especifica como una matriz de objetos incrustados, donde cada objeto es una instancia de la clase [**\_ \_ NTLMUser9X**](--ntlmuser9x.md) . Esto funciona de forma similar al descriptor de seguridad, pero es más limitado. No se admiten grupos y no hay ningún control sobre el acceso local, ya que el usuario local siempre tiene acceso completo. Se permiten las entradas de control de acceso (ACE) deny y allow y, debido a ello, el orden de ACE es importante en la lista de control de acceso discrecional (DACL). Para obtener más información, vea [orden de las ACE en una DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Set9XUserList(
  [in] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*UL* \[ de\]
</dt> <dd>

Matriz de usuarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor HRESULT** que indica el estado de la llamada al método. En la lista siguiente se muestran los valores devueltos que son significativos para **Set9XUserList**. En el caso de las aplicaciones de scripting y Visual Basic, el resultado se puede obtener de [Parameters. ReturnValue](parsing-outparameters-objects.md). Para obtener más información, consulte [construir objetos Parameters y analizar objetos Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**WBEM \_ E \_ método \_ deshabilitado**
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

[**\_\_SystemSecurity:: obtiene**](--systemsecurity-getsd.md)
</dt> <dt>

[**\_\_SystemSecurity:: establecido**](--systemsecurity-setsd.md)
</dt> <dt>

[**ACE de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**SecurityDescriptor de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Proteger los espacios de nombres de WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Constantes de seguridad de WMI](wmi-security-constants.md)
</dt> </dl>

 

