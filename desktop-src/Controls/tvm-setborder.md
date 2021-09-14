---
title: TVM_SETBORDER mensaje (Commctrl.h)
description: Establece el tamaño del borde para los elementos de un control de vista de árbol. Puede enviar el mensaje explícitamente o mediante la macro \_ TreeView SetBorder.
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
ms.openlocfilehash: 6b4401959e2579caab7f2cb4b6eed1ea34481ffa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165658"
---
# <a name="tvm_setborder-message"></a>Mensaje \_ SETBORDER de TVM

**Diseñado para uso interno; no se recomienda para su uso en aplicaciones.**

Establece el tamaño del borde para los elementos de un control de vista de árbol. Puede enviar el mensaje explícitamente o mediante la macro [**\_ TreeView SetBorder.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)

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

Devuelve un **valor LONG** que contiene el tamaño del borde anterior, en píxeles. El [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el tamaño anterior del borde horizontal y [**el HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene el tamaño anterior del borde vertical.

## <a name="remarks"></a>Observaciones

**Advertencia de seguridad:** El uso de este mensaje podría poner en peligro la seguridad del programa.

El borde del elemento se establece solo con fines de espaciado. Una configuración correcta desencadena un recálculo de las barras de desplazamiento.

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
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TreeView \_ SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
</dt> </dl>

 

