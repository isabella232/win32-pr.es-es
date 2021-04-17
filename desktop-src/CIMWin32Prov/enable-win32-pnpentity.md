---
description: Habilita este Plug and Play dispositivo.
ms.assetid: 8f2096c4-03b4-4005-9b97-0086f2b41080
ms.tgt_platform: multiple
title: Método enable de la clase Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.Enable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f64c833a29f4df3b353a7e9782ffea39396cece
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659489"
---
# <a name="enable-method-of-the-win32_pnpentity-class"></a>Método enable de la \_ clase Win32 PnPEntity

Habilita este Plug and Play dispositivo.

## <a name="syntax"></a>Sintaxis


```mof
Uint32 Enable(
  [out] boolean rebootNeeded
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rebootNeeded* \[ enuncia\]
</dt> <dd>

Indica si es necesario reiniciar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ PnPEntity**](win32-pnpentity.md)
</dt> </dl>

 

 




