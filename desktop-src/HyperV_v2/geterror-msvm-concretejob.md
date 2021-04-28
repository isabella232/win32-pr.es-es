---
description: 'Método GetError de la Msvm_ConcreteJob clase : recupera el objeto de error para el trabajo, si existe alguno.'
ms.assetid: 7E810CBE-F18F-4EFA-B52E-631CD071D136
title: Método GetError de la Msvm_ConcreteJob clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c222a7091550b5ee831330f100292549e31ce5ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112193"
---
# <a name="geterror-method-of-the-msvm_concretejob-class"></a>Método GetError de la clase ConcreteJob de \_ Msvm

Recupera el objeto de error para el trabajo, si existe uno. Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve un [**objeto \_ cim error.**](/previous-versions//cc150671(v=vs.85)) Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque un cliente ha finalizado el trabajo, se devuelve una instancia **\_ de error** de CIM.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Error* \[ out\]
</dt> <dd>

Tipo: **cadena**

Si el estado operativo del trabajo no es 2 (correcto), este método devuelve una instancia incrustada de la clase Error de [**Msvm, \_**](msvm-error.md) en formato CIM-XML. Si el estado operativo del trabajo es 2 (correcto), se **devuelve Null.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**El estado es desconocido** (32771)
</dt> <dt>

**Tiempo de** espera (32772)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**Sistema en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está disponible** (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> </dl>

## <a name="remarks"></a>Comentarios

El acceso a [**la clase \_ Msvm ConcreteJob**](msvm-concretejob.md) podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8 solo \[ aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Msvm \_ ConcreteJob**](msvm-concretejob.md)
</dt> </dl>

 

