---
title: Método ISoftKbd CreateSoftKeyboardLayoutFromXMLFile (Softkbdc. h)
description: El método ISoftKbd CreateSoftKeyboardLayoutFromXMLFile crea una distribución de teclado en pantalla a partir del archivo XML especificado.
ms.assetid: e665adab-1d75-4e41-87bf-c8ce0f7a0399
keywords:
- Método CreateSoftKeyboardLayoutFromXMLFile marco de trabajo de servicios de texto
- Método CreateSoftKeyboardLayoutFromXMLFile marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método CreateSoftKeyboardLayoutFromXMLFile
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
ms.openlocfilehash: 9252db845c5e1cc732adc295e1989fee83d4ac6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686096"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromxmlfile-method"></a>ISoftKbd:: CreateSoftKeyboardLayoutFromXMLFile (método)

El método **ISoftKbd:: CreateSoftKeyboardLayoutFromXMLFile** crea una distribución de teclado en pantalla a partir del archivo XML especificado.

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

*lpszKeyboardDesFile* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en cero que indica el nombre del archivo XML.

</dd> <dt>

*szFileStrLen* \[ de\]
</dt> <dd>

Cadena terminada en cero que indica la longitud del archivo XML.

</dd> <dt>

*pdwLayoutCookie* \[ enuncia\]
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

[**ISoftKbd::CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> </dl>

 

 





