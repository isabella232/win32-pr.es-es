---
description: Obtiene un valor que indica si el sistema de claves especificado admite el tipo de medio especificado.
ms.assetid: 6f4f50db-e491-46c2-a8b2-1b8e51033b5b
title: 'IMFMediaEngineClassFactoryEx:: IsTypeSupported (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineClassFactoryEx.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 92bf3d64d36c043e9e33b897294ff74a3fda0445
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697912"
---
# <a name="imfmediaengineclassfactoryexistypesupported-method"></a>IMFMediaEngineClassFactoryEx:: IsTypeSupported (método)

Obtiene un valor que indica si el sistema de claves especificado admite el tipo de medio especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsTypeSupported(
   BSTR type,
   BSTR keySystem,
   BOOL *isSupported
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*type* 
</dt> <dd>

Tipo MIME para el que se va a comprobar la compatibilidad.

</dd> <dt>

*keySystem* 
</dt> <dd>

Sistema de claves para el que se va a comprobar la compatibilidad.

</dd> <dt>

*isSupported* 
</dt> <dd>

**true** si el tipo es compatible con *keySystem*; en caso contrario, **false.**

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

[**IMFMediaEngineClassFactoryEx**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex)
</dt> </dl>

 

 




