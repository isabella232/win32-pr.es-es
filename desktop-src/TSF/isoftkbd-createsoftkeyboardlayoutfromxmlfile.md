---
title: Método ISoftKbd CreateSoftKeyboardLayoutFromXMLFile (Softkbdc.h)
description: El método ISoftKbd CreateSoftKeyboardLayoutFromXMLFile crea un diseño de teclado flexible a partir del archivo XML especificado.
ms.assetid: e665adab-1d75-4e41-87bf-c8ce0f7a0399
keywords:
- Método CreateSoftKeyboardLayoutFromXMLFile Text Services Framework
- Método CreateSoftKeyboardLayoutFromXMLFile Text Services Framework , interfaz ISoftKbd
- Interfaz ISoftKbd Text Services Framework , método CreateSoftKeyboardLayoutFromXMLFile
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromXMLFile
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b53d4ddeabdf343270664e2d65e17d44aeb7ba8f05a23d6f759a51fcc8e99579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877913"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromxmlfile-method"></a>ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile (método)

El **método ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile** crea un diseño de teclado flexible a partir del archivo XML especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateSoftKeyboardLayoutFromXMLFile(
  [in]  WCHAR *lpszKeyboardDesFile,
  [in]  INT   szFileStrLen,
  [out] DWORD *pdwLayoutCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszKeyboardDesFile* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en cero que indica el nombre del archivo XML.

</dd> <dt>

*szFileStrLen* \[ En\]
</dt> <dd>

Cadena terminada en cero que indica la longitud del archivo XML.

</dd> <dt>

*pdwLayoutCookie* \[ out\]
</dt> <dd>

Puntero al búfer en el que este método recupera una cookie de diseño de teclado flexible.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Valor                                                                                        | Descripción                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Método realizado correctamente.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o varios parámetros no son válidos.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> </dl>

 

 





