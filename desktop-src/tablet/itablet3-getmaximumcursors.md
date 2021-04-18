---
description: El método GetMaximumCursors recupera el número máximo de cursores que admite un dispositivo de tableta gráfica.
ms.assetid: 5a43d792-e64c-4506-9792-31efe0885959
title: 'ITablet3:: GetMaximumCursors (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.GetMaximumCursors
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7c40184d35ac1d42cb5f5e845396b40efc2d928e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720584"
---
# <a name="itablet3getmaximumcursors-method"></a>ITablet3:: GetMaximumCursors (método)

El método **GetMaximumCursors** recupera el número máximo de cursores que admite un dispositivo de tableta gráfica.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMaximumCursors(
   ULONG *pMaximumCursors
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMaximumCursors* 
</dt> <dd>

Número máximo de entradas que admite el dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve \_ si es correcto; de lo contrario, devuelve un código de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITablet3**](itablet3.md)
</dt> </dl>

 

 




