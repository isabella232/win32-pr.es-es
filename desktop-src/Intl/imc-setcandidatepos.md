---
description: Indica a una ventana de IME que establezca la posición de la ventana candidata. Para enviar este comando, la aplicación usa el mensaje \_ WM IME \_ CONTROL con la configuración de parámetros que se muestra a continuación.
ms.assetid: 7a2f9958-4a4e-462a-9737-e7796fd90216
title: IMC_SETCANDIDATEPOS comando (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ac05890e4c720c5b671faa7f20a68a96b24a23
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063129"
---
# <a name="imc_setcandidatepos-command"></a>Comando \_ SETCANDIDATEPOS de IMC

Indica a una ventana de IME que establezca la posición de la ventana candidata. Para enviar este comando, la aplicación usa el mensaje [**\_ WM IME \_ CONTROL**](wm-ime-control.md) con la configuración de parámetros que se muestra a continuación.


```C++
LRESULT IMC_SETCANDIDATEPOS
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Establezca en IMC \_ SETCANDIDATEPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Puntero a una [**estructura CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) que contiene la coordenada x y la coordenada y de la ventana candidatos. La aplicación debe establecer el **miembro dwIndex** de esta estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se realiza correctamente o un valor distinto de cero en caso contrario.

## <a name="remarks"></a>Observaciones

Este comando está pensado para aplicaciones que muestran caracteres de composición por sí solas, pero usan la ventana IME para mostrar candidatos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>Imm.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Comandos del Administrador de métodos de entrada](input-method-manager-commands.md)
</dt> <dt>

[**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[**WM \_ IME \_ CONTROL**](wm-ime-control.md)
</dt> </dl>

 

 




