---
description: Indica a una ventana del IME que obtenga la posición de la ventana candidata. Para enviar este comando, la aplicación usa el mensaje de control de IME de WM \_ \_ con la configuración de parámetros que se muestra a continuación.
ms.assetid: e582dbc2-8081-424c-a972-1a182a477293
title: Comando IMC_GETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb5cd143bf45f9bdb37be4cbe3078a483f53db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653111"
---
# <a name="imc_getcandidatepos-command"></a>\_Comando IMC GETCANDIDATEPOS

Indica a una ventana del IME que obtenga la posición de la ventana candidata. Para enviar este comando, la aplicación usa el mensaje de [**\_ \_ control de IME de WM**](wm-ime-control.md) con la configuración de parámetros que se muestra a continuación.


```C++
LRESULT IMC_GETCANDIDATEPOS
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Establezca en IMC \_ GETCANDIDATEPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Puntero a una estructura [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) que contiene la posición de la ventana candidata.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se realiza correctamente, o un valor distinto de cero en caso contrario.

## <a name="remarks"></a>Observaciones

Dado que el IME puede ajustar la posición de una ventana candidata, una aplicación utiliza este comando para obtener la posición real a fin de decidir si se debe cambiar la posición de la ventana. La posición recuperada se encuentra en coordenadas de ventana relativas a la ventana que tiene el foco de entrada actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>IMM. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Comandos del administrador de métodos de entrada](input-method-manager-commands.md)
</dt> <dt>

[**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> </dl>

 

 




