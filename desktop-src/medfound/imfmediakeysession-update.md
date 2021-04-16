---
description: Pasa un valor de clave con los datos asociados requeridos por el módulo de descifrado de contenido para el sistema de claves especificado.
ms.assetid: 29e66037-5f18-4724-b6f2-d85555e6af69
title: 'IMFMediaKeySession:: Update (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Update
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 15bc06523f0cf9a7dc433381dd596cea89608ce7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670091"
---
# <a name="imfmediakeysessionupdate-method"></a>IMFMediaKeySession:: Update (método)

Pasa un valor de clave con los datos asociados requeridos por el módulo de descifrado de contenido para el sistema de claves especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Update(
   const BYTE  *key,
         DWORD cb
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*key* 
</dt> <dd></dd> <dt>

*CB* 
</dt> <dd>

El recuento en bytes de la *clave*.

</dd> </dl>

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

[**IMFMediaKeySession**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




