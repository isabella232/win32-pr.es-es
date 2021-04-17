---
title: IConfigAsfWriter2 SetParam, método
description: El método SetParam establece el valor del parámetro de configuración de filtro especificado.
ms.assetid: b8067fb2-c379-4b26-b4f7-c790604e3edc
keywords:
- Método SetParam formato de Windows Media
- Método SetParam formato de Windows Media, interfaz IConfigAsfWriter2
- Interfaz IConfigAsfWriter2 formato de Windows Media, método SetParam
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.SetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f123bf11c8297f3a7ce0d4b0047874d8d7b31b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695692"
---
# <a name="iconfigasfwriter2setparam-method"></a>IConfigAsfWriter2:: SetParam (método)

El método **SetParam** establece el valor del parámetro de configuración de filtro especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetParam(
  [in] DWORD dwParam,
  [in] DWORD dwParam1,
  [in] DWORD dwParam2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwParam* \[ de\]
</dt> <dd>

Especifica el parámetro que se va a establecer. Debe ser un valor definido en la enumeración de [ \_ \_ \_ parámetros AM ASFWRITERCONFIG](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .

</dd> <dt>

*dwParam1* \[ de\]
</dt> <dd>

Especifica el valor que se va a asignar al parámetro *dwParam* .

</dd> <dt>

*dwParam2* \[ de\]
</dt> <dd>

No se utiliza; debe ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve S \_ correcto. Si se produce un error, devuelve un código de error **HRESULT** .

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2:: GetParam**](iconfigasfwriter2-getparam.md)
</dt> </dl>

 

 