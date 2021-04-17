---
description: Crea un objeto de sesión de clave multimedia con los datos de inicialización y los datos personalizados especificados. .
ms.assetid: 9f11433c-7cff-4a59-9d4a-7f4b56ba62cf
title: 'IMFMediaKeys:: CreateSession (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.CreateSession
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 89d3abce0c1c15d472f7008fa0ef2c5f27bba6ad
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697967"
---
# <a name="imfmediakeyscreatesession-method"></a>IMFMediaKeys:: CreateSession (método)

Crea un objeto de sesión de clave multimedia con los datos de inicialización y los datos personalizados especificados. .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateSession(
         BSTR                     mimeType,
   const BYTE                     *initData,
         DWORD                    cb,
   const BYTE                     *customData,
         DWORD                    cbCustomData,
         IMFMediaKeySessionNotify *notify,
         IMFMediaKeySession       **ppSession
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mimeType* 
</dt> <dd>

El tipo MIME del contenedor multimedia utilizado para el contenido.

</dd> <dt>

*initData* 
</dt> <dd>

Los datos de inicialización del sistema de claves.

</dd> <dt>

*CB* 
</dt> <dd>

El recuento en bytes de *initData*.

</dd> <dt>

*customData* 
</dt> <dd>

Datos personalizados enviados al sistema de claves.

</dd> <dt>

*cbCustomData* 
</dt> <dd>

El recuento en bytes de *cbCustomData*.

</dd> <dt>

*notificar a* 
</dt> <dd>

notificar a

</dd> <dt>

*ppSession* 
</dt> <dd>

La sesión de la clave multimedia.

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

[**IMFMediaKeys**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




