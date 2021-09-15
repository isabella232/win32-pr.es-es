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
ms.openlocfilehash: 92bf3d64d36c043e9e33b897294ff74a3fda0445
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468751"
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



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFMediaEngineClassFactoryEx**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex)
</dt> </dl>

 

 




