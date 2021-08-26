---
description: El método \_ get Alpha recupera el valor alfa de toda la imagen.
ms.assetid: ce891149-e964-4239-aeef-c9f4a8354563
title: Método IDxtAlphaSetter::get_Alpha (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 054e2a1745f96dc4d6ea846bed0448948fae8407dd6ab44d2796742e405f2e1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051975"
---
# <a name="idxtalphasetterget_alpha-method"></a>Método IDxtAlphaSetter::get \_ Alpha

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `get_Alpha` método recupera el valor alfa de toda la imagen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Alpha(
  [out, retval] long *pAlpha
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAlpha* \[ out, retval\]
</dt> <dd>

Recibe el valor alfa. Este valor alfa se aplicará a toda la imagen de destino. Un valor negativo indica que no se establece ningún valor alfa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                               | Descripción                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | **Argumento de** puntero NULL<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Correcto<br/>                   |



 

## <a name="remarks"></a>Comentarios

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDxtAlphaSetter (interfaz)**](idxtalphasetter.md)
</dt> </dl>

 

 




