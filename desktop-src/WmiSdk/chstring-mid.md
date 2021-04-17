---
description: El método Mid extrae una subcadena de longitud nCount caracteres de una cadena CHString, comenzando en la posición Nprimer (basada en cero). El método devuelve una copia de la subcadena extraída.
audience: developer
ms.assetid: 2036813b-f991-4ca3-95d3-8bbe858aae09
ms.tgt_platform: multiple
title: 'Métodos CHString:: MID (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5d05259128f80bcb21d00144d19002ca58ce39c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716289"
---
# <a name="chstringmid-methods"></a>CHString:: MID (métodos)

\[La clase [**CHString**](chstring.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

El método **Mid** extrae una subcadena de longitud *nCount* caracteres de una cadena [**CHString**](chstring.md) , comenzando en la posición *nprimer* (basada en cero). El método devuelve una copia de la subcadena extraída.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                        | Descripción                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [**MID (int, int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int)) | Extrae una subcadena de la longitud y el punto inicial especificados.<br/> |
| [**MID (int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))         | Extrae una subcadena que comienza en int.<br/>                        |



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
