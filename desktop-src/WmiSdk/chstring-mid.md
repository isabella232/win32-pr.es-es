---
description: El método Mid extrae una subcadena de longitud de caracteres nCount de una cadena CHString, empezando en la posición nFirst (base cero). El método devuelve una copia de la subcadena extraída.
audience: developer
ms.assetid: 2036813b-f991-4ca3-95d3-8bbe858aae09
ms.tgt_platform: multiple
title: Métodos CHString::Mid (ChString.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: cbe5b7fc6e3f0d4130e106217c46c82202c230f180dd4c90d09f90073dee08ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319847"
---
# <a name="chstringmid-methods"></a>Métodos CHString::Mid

\[La [**clase CHString**](chstring.md) forma parte del marco de proveedores WMI que ahora se considera en estado final y no habrá más desarrollos, mejoras o actualizaciones disponibles para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

El **método Mid** extrae una subcadena de longitud de caracteres *nCount* de una cadena [**CHString,**](chstring.md) empezando en la *posición nFirst* (base cero). El método devuelve una copia de la subcadena extraída.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                        | Descripción                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [**Mid(int,int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int)) | Extrae una subcadena de longitud y punto inicial especificados.<br/> |
| [**Mid(int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))         | Extrae una subcadena que comienza en int.<br/>                        |



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
