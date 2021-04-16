---
description: Se utiliza para indicar que se ha producido un error con el búfer de origen.
ms.assetid: a7187b7a-0090-4380-82bb-a7f72d54232e
title: 'IMFSourceBufferNotify:: OnError (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBufferNotify.OnError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 8b5f48c3517eb62b0a70acb9cbb28a5ecf7c90cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705805"
---
# <a name="imfsourcebuffernotifyonerror-method"></a>IMFSourceBufferNotify:: OnError (método)

Se utiliza para indicar que se ha producido un error con el búfer de origen.

## <a name="syntax"></a>Sintaxis


```C++
void OnError(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HR* \[ de\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFSourceBufferNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify)
</dt> </dl>

 

 




