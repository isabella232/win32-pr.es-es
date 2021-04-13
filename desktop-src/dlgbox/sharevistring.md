---
title: Mensaje SHAREVISTRING (commdlg. h)
description: Un cuadro de diálogo abrir o guardar como envía el mensaje registrado SHAREVISTRING al procedimiento de enlace, OFNHookProc, si se produce una infracción de uso compartido para el archivo seleccionado cuando el usuario hace clic en el botón Aceptar.
ms.assetid: 53884497-4872-4aa8-b56e-2bb98df58fed
keywords:
- Cuadros de diálogo de mensaje de SHAREVISTRING
topic_type:
- apiref
api_name:
- SHAREVISTRING
- SHAREVISTRINGA
- SHAREVISTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23c17280ad1156e35f7e0f503816c07645cf4f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491872"
---
# <a name="sharevistring-message"></a>Mensaje SHAREVISTRING

\[A partir de Windows Vista, los cuadros de diálogo **abrir** y **Guardar como** común se han sustituido por el [cuadro de diálogo de elementos comunes](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)). Se recomienda usar la API de cuadros de diálogo de elementos comunes en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo comunes.\]

Un cuadro de diálogo **abrir** o **Guardar como** envía el mensaje registrado **SHAREVISTRING** al procedimiento de enlace, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), si se produce una infracción de uso compartido para el archivo seleccionado cuando el usuario hace clic en el botón **Aceptar** .


```C++
#define SHAREVISTRING TEXT("commdlg_ShareViolation")
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) . El miembro **lpstrFile** de esta estructura contiene el nombre de archivo que causó la infracción de uso compartido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El procedimiento de enlace debe devolver uno de los valores siguientes para indicar cómo el cuadro de diálogo debe controlar la infracción de uso compartido.



| Código o valor devuelto                                                                                                                                           | Descripción                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt> </dl> | Aceptar el nombre de archivo<br/>                                                                                            |
| <dl> <dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt> </dl>      | Rechace el nombre de archivo, pero no advierta al usuario. La aplicación es responsable de mostrar un mensaje de advertencia.<br/> |
| <dl> <dt>**OFN \_ SHAREWARN**</dt> <dt>0</dt> </dl>        | Rechace el nombre de archivo y muestre un mensaje de advertencia (el mismo resultado que si no hubiera ningún procedimiento de enlace).<br/>       |



 

## <a name="remarks"></a>Observaciones

El procedimiento de enlace debe especificar la constante **SHAREVISTRING** en una llamada a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener el identificador del mensaje enviado por el cuadro de diálogo.

El cuadro de diálogo solo envía el mensaje registrado de **SHAREVISTRING** si no especificó la marca **\_ SHAREAWARE de OFN** en el miembro **Flags** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) al crear el cuadro de diálogo.

Si el procedimiento de enlace devuelve un valor no definido, el cuadro de diálogo responde como si se devolviera **OFN \_ SHAREWARN** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **SHAREVISTRINGW** (Unicode) y **SHAREVISTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**SHAREVIOLATION de CDN \_**](cdn-shareviolation.md)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Vista**
</dt> <dt>

[Biblioteca de cuadros de diálogo comunes](common-dialog-box-library.md)
</dt> </dl>

 

