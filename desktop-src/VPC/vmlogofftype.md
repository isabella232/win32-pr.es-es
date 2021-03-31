---
title: Enumeración VMLogoffType (VPCCOMInterfaces. h)
description: Especifica cómo apagar una máquina virtual.
ms.assetid: 3a2965e3-2637-4677-b487-98d2b508672c
keywords:
- Enumeración de VMLogoffType Virtual PC
topic_type:
- apiref
api_name:
- VMLogoffType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2311736115390d807058bbfc54c24e7f9e9654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079328"
---
# <a name="vmlogofftype-enumeration"></a>Enumeración VMLogoffType

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Especifica cómo apagar una máquina virtual (VM).

## <a name="syntax"></a>Sintaxis


```C++
typedef enum  { 
  vmLogoff_Normal    = 0,
  vmLogoff_Forced    = 1,
  vmLogoff_External  = 2
} VMLogoffType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmLogoff_Normal"></span><span id="vmlogoff_normal"></span><span id="VMLOGOFF_NORMAL"></span>**vmLogoff \_ normal**
</dt> <dd>

El cierre de sesión en la máquina virtual invitada era normal.

</dd> <dt>

<span id="vmLogoff_Forced"></span><span id="vmlogoff_forced"></span><span id="VMLOGOFF_FORCED"></span>**vmLogoff \_ forzada**
</dt> <dd>

Se forzó el cierre de sesión en la máquina virtual invitada.

</dd> <dt>

<span id="vmLogoff_External"></span><span id="vmlogoff_external"></span><span id="VMLOGOFF_EXTERNAL"></span>**vmLogoff \_ externo**
</dt> <dd>

El cierre de sesión en la máquina virtual invitada se realizó con el método [**IVMGuestOS:: Logoff**](ivmguestos-logoff.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachine::ShutdownActionOnQuit**](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

