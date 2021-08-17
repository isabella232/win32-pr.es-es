---
description: El método GetStretchMode recupera el modo stretch. El modo de ajuste determina cómo se representa un origen de vídeo si su tamaño no coincide con las dimensiones de salida.
ms.assetid: d9a3d283-edb5-40be-b877-69cb23462afa
title: Método IAMTimelineSrc::GetStretchMode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 53be58df0315c4a03c62369f746efa510c2024fa030c3bef75eb4ff08505b1c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952914"
---
# <a name="iamtimelinesrcgetstretchmode-method"></a>IamTimelineSrc::GetStretchMode (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetStretchMode` método recupera el modo de ajuste. El modo de ajuste determina cómo se representa un origen de vídeo si su tamaño no coincide con las dimensiones de salida.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStretchMode(
   int *pnStretchMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pnStretchMode* 
</dt> <dd>

Recibe una marca que indica el modo de ajuste actual. Para obtener una lista de valores posibles, vea [**Cambiar el tamaño de las marcas**](resize-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

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

[**IamTimelineSrc (interfaz)**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




