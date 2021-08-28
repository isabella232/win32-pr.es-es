---
description: 'Operador de resta de clase WBEMTime (&\# 8211;) se ha sobrecargado para:'
audience: developer
ms.assetid: 0fa51aab-7ea2-4af7-bb12-1646388b0405
ms.tgt_platform: multiple
title: Operadores WBEMTime::operator- (WbemTime.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 7748020c1dcf1e332384c3a29c18b37da53e020f42d6cb608d9bf3233608aaaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120755"
---
# <a name="wbemtimeoperator--operators"></a>Operadores WBEMTime::operator-

\[La [**clase WBEMTime**](wbemtime.md) forma parte del marco de proveedores WMI que ahora se considera en estado final y no habrá más desarrollos, mejoras o actualizaciones disponibles para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

El operador de resta de clase [**WBEMTime**](wbemtime.md) ( ) se ha sobrecargado para:

-   Resta un intervalo de tiempo del tiempo de un objeto para generar un nuevo objeto de hora que contenga la hora resultante.
-   Resta un tiempo del tiempo del objeto para generar un nuevo objeto de intervalo de tiempo que contenga la diferencia entre las dos veces.

### <a name="overload-list"></a>Lista de sobrecarga



| Operador                                                                         | Descripción                                                                      |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**operator-(WBEMTime&)**](/windows/win32/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize)         | Resta **un WBEMTime** de **un WBEMTime**.<br/>                         |
| [**operator-(WBEMTimeSpan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_)) | Resta un [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) de **un WBEMTime**.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>WbemTime.h</dt> </dl>                                                                         |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
