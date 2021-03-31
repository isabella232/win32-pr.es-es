---
description: Cada uno de los constructores siguientes Inicializa un nuevo objeto CHString con los datos especificados.
audience: developer
ms.assetid: d49e1600-d5d4-4c44-81c5-1b8c53b768de
ms.tgt_platform: multiple
title: 'Constructores CHString:: CHString (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 711d2f28680a9f273ff808876e30e92f66336b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277126"
---
# <a name="chstringchstring-constructors"></a>Constructores CHString:: CHString

\[La clase [**CHString**](chstring.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

Cada uno de los constructores siguientes Inicializa un nuevo objeto [**CHString**](chstring.md) con los datos especificados.

### <a name="overload-list"></a>Lista de sobrecarga



| Constructor                                                                        | Descripción                                                  |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------|
| [**CHString()**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                          | Crea un objeto CHString vacío.<br/>                 |
| [**CHString (LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))                              | Se inicializa con el valor de LPCSTR.<br/>                |
| [**CHString (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))                            | Se inicializa con el valor de LPCWSTR.<br/>               |
| [**CHString (WCHAR, int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))                        | Inicializa con las copias int del valor WCHAR.<br/>   |
| [**CHString (LPCWSTR, int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))                    | Inicializa con las copias int del valor de LPCWSTR.<br/> |
| [**CHString (const CHString&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))            | Replica el parámetro CHString.<br/>                |
| [**CHString (const sin signo \* )**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar)) | Se inicializa con el valor al que apunta char \* .<br/>  |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                |
| Encabezado<br/>                   | <dl> <dt>ChString. h (incluye FwCommon. h)</dt> </dl>                                                    |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
