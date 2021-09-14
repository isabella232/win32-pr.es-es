---
title: Mensaje SHAREVISTRING (Commdlg.h)
description: Un cuadro de diálogo Abrir o Guardar como envía el mensaje registrado de SHAREVISTRING al procedimiento de enlace, OFNHookProc, si se produce una infracción de uso compartido para el archivo seleccionado cuando el usuario hace clic en el botón Aceptar.
ms.assetid: 53884497-4872-4aa8-b56e-2bb98df58fed
keywords:
- Cuadros de diálogo del mensaje SHAREVISTRING
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
ms.openlocfilehash: 043bed9edd08269e4e030482cbd44debea3a3695
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966403"
---
# <a name="sharevistring-message"></a>Mensaje SHAREVISTRING

\[A partir Windows Vista,  los  cuadros de diálogo Abrir y Guardar como comunes se han reemplazado por el cuadro [de diálogo Elemento común](../shell/common-file-dialog.md). Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo común.\]

Un **cuadro** de **diálogo** Abrir o Guardar como envía el mensaje registrado de **SHAREVISTRING** al procedimiento de enlace, [*OFNHookProc,*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)si se produce una infracción de uso compartido para el archivo seleccionado cuando el usuario hace clic en el **botón** Aceptar.


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

Puntero a una [**estructura OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) El **miembro lpstrFile** de esta estructura contiene el nombre de archivo que produjo la infracción de uso compartido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El procedimiento de enlace debe devolver uno de los siguientes valores para indicar cómo debe controlar el cuadro de diálogo la infracción de uso compartido.



| Código o valor devuelto                                                                                                                                           | Descripción                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt> </dl> | Aceptación del nombre de archivo<br/>                                                                                            |
| <dl> <dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt> </dl>      | Rechace el nombre de archivo, pero no advierte al usuario. La aplicación es responsable de mostrar un mensaje de advertencia.<br/> |
| <dl> <dt>**OFN \_ SHAREWARN**</dt> <dt>0</dt> </dl>        | Rechace el nombre de archivo y muestra un mensaje de advertencia (el mismo resultado que si no hubiera ningún procedimiento de enlace).<br/>       |



 

## <a name="remarks"></a>Observaciones

El procedimiento de enlace debe especificar la **constante SHAREVISTRING** en una llamada a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener el identificador del mensaje enviado por el cuadro de diálogo.

El cuadro de diálogo envía el mensaje registrado **de SHAREVISTRING** solo si no especificó la marca **OFN \_ SHAREAWARE** en el miembro **Flags** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) al crear el diálogo.

Si el procedimiento de enlace devuelve un valor indefinido, el cuadro de diálogo responde como si se hubiera devuelto **OFN \_ SHAREWARN.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **SHAREVISTRINGW** (Unicode) y **SHAREVISTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_CDN SHAREVIOLATION**](cdn-shareviolation.md)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> </dl>

