---
description: Cada uno de los constructores siguientes inicializa un nuevo objeto CHString con los datos especificados.
audience: developer
ms.assetid: d49e1600-d5d4-4c44-81c5-1b8c53b768de
ms.tgt_platform: multiple
title: Constructores CHString::CHString (ChString.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 80ce10988fc335c5a16eff8507346dbcdffd6fa70f75d74fb48d3f84b0e2332b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320053"
---
# <a name="chstringchstring-constructors"></a>Constructores CHString::CHString

\[La [**clase CHString**](chstring.md) forma parte del marco de proveedores WMI que ahora se considera en estado final y no habrá más desarrollos, mejoras o actualizaciones disponibles para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

Cada uno de los constructores siguientes inicializa un nuevo [**objeto CHString**](chstring.md) con los datos especificados.

### <a name="overload-list"></a>Lista de sobrecarga



| Constructor                                                                        | Descripción                                                  |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------|
| [**CHString()**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                          | Crea un objeto CHString vacío.<br/>                 |
| [**CHString(LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))                              | Inicializa con el valor LPCSTR.<br/>                |
| [**CHString(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))                            | Inicializa con el valor LPCWSTR.<br/>               |
| [**CHString(WCHAR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))                        | Inicializa con copias int del valor WCHAR.<br/>   |
| [**CHString(LPCWSTR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))                    | Inicializa con copias int del valor LPCWSTR.<br/> |
| [**CHString(const CHString&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))            | Replica el parámetro CHString.<br/>                |
| [**CHString(const unsigned char \* )**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar)) | Inicializa con el valor al que apunta char \* .<br/>  |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>ChString.h (incluya FwCommon.h)</dt> </dl>                                                    |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
