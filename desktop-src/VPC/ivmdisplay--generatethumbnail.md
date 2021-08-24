---
title: Método _GenerateThumbnail IVMDisplay (VPCCOMInterfaces.h)
description: Recupera una matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual. | Método de _GenerateThumbnail IVMDisplay (VPCCOMInterfaces.h)
ms.assetid: c97bb0ff-55cd-491f-a706-0ba15c9a6b54
keywords:
- _GenerateThumbnail virtual PC
- _GenerateThumbnail método Virtual PC , interfaz IVMDisplay
- IVMDisplay interface Virtual PC , _GenerateThumbnail método
topic_type:
- apiref
api_name:
- IVMDisplay._GenerateThumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5decd1b3c55ab6513408a81eb37d422fac495334fb545c4cad4806050a8af7b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654375"
---
# <a name="ivmdisplay_generatethumbnail-method"></a>IVMDisplay:: \_ Método GenerateThumbnail

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera una matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT _GenerateThumbnail(
  [out] unsigned long thumbnailImage[3072]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*thumbnailImage* \[ out\]
</dt> <dd>

Matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                 | Descripción                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>        |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



 

## <a name="remarks"></a>Comentarios

Esta interfaz devuelve la miniatura de forma más eficaz que la [**propiedad Thumbnail,**](ivmdisplay-thumbnail.md) pero no se puede usar desde clientes de scripting. La miniatura siempre tiene 64 píxeles de ancho por 48 píxeles de alto. Cada píxel es de 32 bits, donde los 8 bits superiores representan el valor azul del píxel, los 8 bits siguientes representan el valor verde del píxel y los 8 bits siguientes representan el valor rojo del píxel. Los primeros 64 elementos de la matriz son la primera fila de la miniatura, los 64 elementos siguientes son la segunda fila, y así sucesivamente. Este método devuelve una matriz estática de píxeles, que es más eficaz que devolver **una SAFEARRAY** de valores **VARIANT,** pero no es compatible con los clientes de scripting.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMDisplay se define como \_ 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

