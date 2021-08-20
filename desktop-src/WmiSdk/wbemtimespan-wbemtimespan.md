---
description: El constructor de la clase WBEMTimeSpan crea un objeto de intervalo de tiempo. El constructor está sobrecargado.
audience: developer
ms.assetid: 337dc247-9904-457a-a1f3-e1cf29b61126
ms.tgt_platform: multiple
title: CONSTRUCTORES WBEMTimeSpan::WbemTimeSpan (WbemTime.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: cedd30f887b7cb789f44f06ab2c6d6b93e3d7c4723c7e0189764164bdbb43d6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118107276"
---
# <a name="wbemtimespanwbemtimespan-constructors"></a>WBEMTimeSpan::WbemTimeSpan constructores

\[La [**clase WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) forma parte del marco de proveedores WMI que ahora se considera en estado final y no habrá más desarrollos, mejoras o actualizaciones disponibles para problemas relacionados con la seguridad que afectan a estas bibliotecas. Las [API de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el nuevo desarrollo.\]

El constructor **de la clase WBEMTimeSpan** crea un objeto de intervalo de tiempo. El constructor está sobrecargado.

### <a name="overload-list"></a>Lista de sobrecarga



| Constructor                                                                                                 | Descripción                                                                  |
|:------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**WBEMTimeSpan()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))                                                      | Crea un objeto de intervalo de tiempo sin inicializar.<br/>                        |
| [**WBEMTimeSpan(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))                                               | Inicializa el nuevo objeto de intervalo de tiempo en el valor del parámetro .<br/>   |
| [**WBEMTimeSpan(int,int,int,int,int,int,int)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(int_int_int_int_int_int_int)) | Inicializa el nuevo objeto de intervalo de tiempo en los valores de los parámetros.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>WbemTime.h</dt> </dl>                                                                         |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
