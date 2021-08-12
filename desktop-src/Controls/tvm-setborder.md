---
title: TVM_SETBORDER mensaje (Commctrl.h)
description: Establece el tamaño del borde de los elementos de un control de vista de árbol. Puede enviar el mensaje explícitamente o mediante la macro TreeView \_ SetBorder.
ms.assetid: 468b46ae-2ab2-4753-a0af-7c644f75ce62
keywords:
- TVM_SETBORDER controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1c8cab133fb654e431638be96301325d68d9743109f84ed8def1ee9cc67c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669660"
---
# <a name="tvm_setborder-message"></a>Mensaje \_ SETBORDER de TVM

**Destinado a uso interno; no se recomienda para su uso en aplicaciones.**

Establece el tamaño del borde de los elementos de un control de vista de árbol. Puede enviar el mensaje explícitamente o mediante la macro [**TreeView \_ SetBorder.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Marcas de acción. Este parámetro puede ser uno o varios de los valores siguientes:



| Value                                                                                                                                                         | Significado                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="TVSBF_XBORDER"></span><span id="tvsbf_xborder"></span><dl> <dt>**TVSBF \_ XBORDER**</dt> </dl> | Aplica el tamaño de borde especificado al lado izquierdo de los elementos del control de vista de árbol. <br/> |
| <span id="TVSBF_YBORDER"></span><span id="tvsbf_yborder"></span><dl> <dt>**TVSBF \_ YBORDER**</dt> </dl> | Aplica el tamaño de borde especificado a la parte superior de los elementos del control de vista de árbol.<br/>        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD es**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un **short** que especifica el tamaño del borde izquierdo, en píxeles. [**HIWORD es**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) un **valor SHORT** que especifica el tamaño del borde superior, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor LONG** que contiene el tamaño del borde anterior, en píxeles. LOWORD [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el tamaño anterior del borde horizontal y [**hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene el tamaño anterior del borde vertical.

## <a name="remarks"></a>Observaciones

**Advertencia de seguridad:** El uso de este mensaje puede poner en peligro la seguridad del programa.

El borde del elemento se establece solo con fines de espaciado. Una configuración correcta desencadena un nuevo cálculo de las barras de desplazamiento.

Es posible que este mensaje no se pueda usar en versiones futuras de Comctl32.dll. Además, este mensaje no está definido en commctrl.h. Agregue las siguientes definiciones a los archivos de origen de la aplicación para usar el mensaje:

``` syntax
#define TVM_SETBORDER (TV_FIRST + 35)
#define TVSBF_XBORDER 0x00000001
#define TVSBF_YBORDER 0x00000002 
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TreeView \_ SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
</dt> </dl>

 

