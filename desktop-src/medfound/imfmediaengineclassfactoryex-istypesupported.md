---
description: Obtiene un valor que indica si el sistema de claves especificado admite el tipo de medio especificado.
ms.assetid: 6f4f50db-e491-46c2-a8b2-1b8e51033b5b
title: MÉTODO IMFMediaEngineClassFactoryEx::IsTypeSupported
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
ms.openlocfilehash: 588a7fdc02fb59a9dc156f9f141b210d36e4cef131bf353d6c98d9c055392a28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118063004"
---
# <a name="imfmediaengineclassfactoryexistypesupported-method"></a>MÉTODO IMFMediaEngineClassFactoryEx::IsTypeSupported

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

Tipo MIME para el que se comprobará la compatibilidad.

</dd> <dt>

*keySystem* 
</dt> <dd>

Sistema clave para el que se comprobará la compatibilidad.

</dd> <dt>

*isSupported* 
</dt> <dd>

**true** si el tipo es compatible con *keySystem*; de lo contrario, **false.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFMediaEngineClassFactoryEx**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex)
</dt> </dl>

 

 




