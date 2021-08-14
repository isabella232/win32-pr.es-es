---
description: El método Find busca en una cadena la primera coincidencia de una subcadena.
audience: developer
ms.assetid: 98a7c5ad-5bc7-4918-b978-45d2b439f250
ms.tgt_platform: multiple
title: Métodos CHString::Find (ChString.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a7f326b202d107dc192683517508446b3c785266c675e5cf27d92577311d453a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319999"
---
# <a name="chstringfind-methods"></a>Métodos CHString::Find

\[La [**clase CHString**](chstring.md) forma parte del marco de proveedores WMI que ahora se considera en estado final y no habrá más desarrollos, mejoras o actualizaciones disponibles para problemas no relacionados con la seguridad que afectan a estas bibliotecas. Las [API de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el nuevo desarrollo.\]

El **método Find** busca en una cadena la primera coincidencia de una subcadena.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                          | Descripción                                             |
|:------------------------------------------------|:--------------------------------------------------------|
| [**Find(WCHAR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))     | Busca el **WSTR** en esta cadena.<br/>    |
| [**Find(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr)) | Busca el **LPCWSTR** en esta cadena.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>ChString.h (include FwCommon.h)</dt> </dl>                                                    |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
