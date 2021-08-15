---
description: El método InsertAt inserta un elemento (o varias copias de un elemento) o todos los elementos de otra matriz en un índice especificado.
audience: developer
ms.assetid: 1d6355bc-7df2-4aa3-8e47-0239d726ed7d
ms.tgt_platform: multiple
title: Métodos CHStringArray::InsertAt (ChStrArr.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 75332e300987233c0a6f3d6755d27fd7c305a7d86fb6cd9a6143c417222c0dcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097255"
---
# <a name="chstringarrayinsertat-methods"></a>Métodos CHStringArray::InsertAt

\[La [**clase CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) forma parte del marco de proveedores WMI que ahora se considera en estado final y no habrá más desarrollos, mejoras o actualizaciones disponibles para problemas no relacionados con la seguridad que afectan a estas bibliotecas. Las [API de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el nuevo desarrollo.\]

El **método InsertAt** inserta un elemento (o varias copias de un elemento) o todos los elementos de otra matriz en un índice especificado.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                               | Descripción                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**InsertAt(int,LPCWSTR,int)**](/previous-versions/windows/desktop/legacy/aa385383(v=vs.85))       | Inserta uno o varios elementos en un índice especificado de una matriz.<br/>                                               |
| [**InsertAt(int,CHStringArray \* )**](/windows/win32/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray)) | Inserta todos los elementos de otra [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) en un índice especificado de una matriz.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>ChStrArr.h (include FwCommon.h)</dt> </dl>                                                    |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray)
</dt> </dl>

�

�
