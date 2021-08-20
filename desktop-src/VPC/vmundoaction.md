---
title: Enumeración VMUndoAction (VPCCOMInterfaces.h)
description: Especifica lo que sucede al deshacer unidades cuando una máquina virtual se apaga o se apaga.
ms.assetid: f8f96fd3-0b2a-40ae-8b2e-b6bcc995dedd
keywords:
- VMUndoAction enumeration Virtual PC
topic_type:
- apiref
api_name:
- VMUndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f62c4ab00b30300b2951a5a6b1c300bf34b1b3797f036f28a66e82dc2cad22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998335"
---
# <a name="vmundoaction-enumeration"></a>Enumeración VMUndoAction

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Especifica lo que sucede al deshacer unidades cuando una máquina virtual se apaga o se apaga.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmUndoAction_Discard  = 0,
  vmUndoAction_Keep     = 1,
  vmUndoAction_Commit   = 2
} VMUndoAction;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**Descarte de \_ vmUndoAction**
</dt> <dd>

Descarte las unidades de deshacer; las unidades primarias permanecen sin cambios.

</dd> <dt>

<span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**vmUndoAction \_ Keep**
</dt> <dd>

Mantenga las unidades de deshacer; las unidades primarias permanecen sin cambios, pero los cambios se mantendrán la próxima vez que se inicie la máquina virtual.

</dd> <dt>

<span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**VmUndoAction \_ Commit**
</dt> <dd>

Confirme los cambios en las unidades primarias.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachine::UndoAction**](ivmvirtualmachine-undoaction.md)
</dt> </dl>

 

