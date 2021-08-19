---
description: El método get \_ AlphaRamp recupera la propiedad de rampa alfa. La rampa alfa es el porcentaje por el que se ajustan los valores alfa de la imagen original. Por ejemplo, si la rampa alfa es 0,5, los valores alfa de la imagen se reducen un 50 %.
ms.assetid: e142a562-2e78-4418-94e9-b41320d4af57
title: Método IDxtAlphaSetter::get_AlphaRamp (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9768ed96f0b40e074fd44de04ca44a8cc17d9de7ce4b75af948975e26b5e3077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952744"
---
# <a name="idxtalphasetterget_alpharamp-method"></a>Método IDxtAlphaSetter::get \_ AlphaRamp

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `get_AlphaRamp` método recupera la propiedad de rampa alfa. La rampa alfa es el porcentaje por el que se ajustan los valores alfa de la imagen original. Por ejemplo, si la rampa alfa es 0,5, los valores alfa de la imagen se reducen un 50 %.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_AlphaRamp(
  [out, retval] double *pAlpha
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAlpha* \[ out, retval\]
</dt> <dd>

Recibe la rampa alfa. Un valor negativo indica que no se ha establecido ninguna rampa alfa.

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

[**Interfaz IDxtAlphaSetter**](idxtalphasetter.md)
</dt> </dl>

 

 




