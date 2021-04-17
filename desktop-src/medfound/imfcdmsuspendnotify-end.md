---
description: La suspensión real está a punto de producirse y no se realizarán más llamadas en el módulo de descifrado de contenido (CDM).
ms.assetid: 7a319fbb-9757-45da-8a8b-51dd48f08464
title: 'IMFCdmSuspendNotify:: end (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFCdmSuspendNotify.End
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 71843b53fa85fded646fe71f2caa463a71c9415f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715883"
---
# <a name="imfcdmsuspendnotifyend-method"></a>IMFCdmSuspendNotify:: end (método)

La suspensión real está a punto de producirse y no se realizarán más llamadas en el módulo de descifrado de contenido (CDM).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT End();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFCdmSuspendNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




