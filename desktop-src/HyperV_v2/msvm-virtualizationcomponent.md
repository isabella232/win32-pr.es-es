---
description: Representa un servicio de microsoft Windows plataforma Hyper-V.
ms.assetid: 309EFE4C-EEA4-454C-943D-CBF99D64FE15
title: Msvm_VirtualizationComponent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponent
- Msvm_VirtualizationComponent.CLSID
- Msvm_VirtualizationComponent.Context
- Msvm_VirtualizationComponent.Enabled
- Msvm_VirtualizationComponent.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab2d2d5652f2969ad20ee70077d23375371e3507991a16b6d5e6dda2245678ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068435"
---
# <a name="msvm_virtualizationcomponent-class"></a>Clase VirtualizationComponent de Msvm \_

Representa un servicio de microsoft Windows plataforma Hyper-V.

La sintaxis siguiente se ha simplificado Managed Object Format (MOF).

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract]
class Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ VirtualizationComponent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ VirtualizationComponent de Msvm** tiene estas propiedades.

<dl> <dt>

**Clsid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

GUID **que** representa el identificador de clase del objeto COM del servicio.

</dd> <dt>

**Contexto**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Experimental**
</dt> </dl>

Contexto en el que se ejecutará el objeto recién creado. Este valor se pasa en el *parámetro dwClsContext* a [**CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) Esta propiedad siempre se establece en 1.

</dd> <dt>

**Habilitado**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**True** es que esta instancia está habilitada y se puede usar para completar las solicitudes de cliente; de lo contrario, **False**. Esta propiedad siempre se establece en **True.**

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Cadena neutra del idioma que identifica de forma única el servicio. Se recomienda el formato siguiente para evitar conflictos de nomenclatura: "versión del \| componente \| de proveedor". Por ejemplo, este nombre representa la versión 1.0 del componente de puerto de red emulado de Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| V1.0".

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a la **clase Msvm \_ VirtualizationComponent** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Fin de compatibilidad de cliente<br/>    | Windows 8.1<br/>                                                                                  |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

