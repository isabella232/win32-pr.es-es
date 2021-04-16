---
title: Método ISoftKbd CreateSoftKeyboardLayoutFromResource (Softkbdc. h)
description: El método ISoftKbd CreateSoftKeybboardLayoutFromResource crea una distribución de teclado en pantalla a partir del recurso especificado.
ms.assetid: c1b2f8bd-8065-426d-9c23-67fa46a33dc8
keywords:
- Método CreateSoftKeyboardLayoutFromResource marco de trabajo de servicios de texto
- Método CreateSoftKeyboardLayoutFromResource marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método CreateSoftKeyboardLayoutFromResource
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromResource
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f454b5d8f3366517d91170d6a92d6a9dbed5764
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686097"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromresource-method"></a>ISoftKbd:: CreateSoftKeyboardLayoutFromResource (método)

El método **ISoftKbd:: CreateSoftKeybboardLayoutFromResource** crea una distribución de teclado en pantalla a partir del recurso especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateSoftKeyboardLayoutFromResource(
  [in]  WCHAR *lpszResFile,
  [in]  WCHAR *lpszResType,
  [in]  WCHAR *lpszXMLResString,
  [out] DWORD *lpdwLayoutCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszResFile* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en cero que indica el nombre del archivo de recursos.

</dd> <dt>

*lpszResType* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en cero que indica el tipo de recurso.

</dd> <dt>

*lpszXMLResString* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en cero que identifica el recurso.

</dd> <dt>

*lpdwLayoutCookie* \[ enuncia\]
</dt> <dd>

Puntero al búfer en el que este método recupera una cookie de distribución de teclado en pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                        | Descripción                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Método realizado correctamente.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o más parámetros no son válidos.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile**](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)
</dt> <dt>

[**ISoftKbd::ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)
</dt> </dl>

 

 





