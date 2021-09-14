---
description: Habilita este Plug and Play dispositivo.
ms.assetid: 8f2096c4-03b4-4005-9b97-0086f2b41080
ms.tgt_platform: multiple
title: Método Enable de la Win32_PnPEntity clase
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062715"
---
# <a name="enable-method-of-the-win32_pnpentity-class"></a>Método Enable de la clase PnPEntity de Win32 \_

Habilita este Plug and Play dispositivo.

## <a name="syntax"></a>Sintaxis


```mof
Uint32 Enable(
  [out] boolean rebootNeeded
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rebootNeeded* \[ out\]
</dt> <dd>

Si se necesita un reinicio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ PnPEntity**](win32-pnpentity.md)
</dt> </dl>

 

 




