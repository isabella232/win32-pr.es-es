---
title: Propiedad IVMDisplay Thumbnail (VPCCOMInterfaces.h)
description: Recupera una matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual. | Propiedad IVMDisplay Thumbnail (VPCCOMInterfaces.h)
ms.assetid: e7b57f16-eec1-4461-acfb-742976eff14a
keywords:
- Propiedad Thumbnail de Virtual PC
- Propiedad thumbnail Virtual PC, interfaz IVMDisplay
- IVMDisplay interface Virtual PC , Propiedad Thumbnail
topic_type:
- apiref
api_name:
- IVMDisplay.Thumbnail
- IVMDisplay.get_Thumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a558a551972bb76558dcd60223d8ddc29783aeaa23e6dbe9263f34642c1c3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473335"
---
# <a name="ivmdisplaythumbnail-property"></a>IVMDisplay::Thumbnail, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera una matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Thumbnail(
  [out, retval] VARIANT *thumbnailImage
);
```



## <a name="property-value"></a>Valor de propiedad

Variante de tipo VT ARRAY VT VARIANT que contiene entradas de tipo \_ VT UI4, una para \| cada píxel de la \_ \_ miniatura.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



## <a name="remarks"></a>Comentarios

Esta interfaz devuelve la miniatura de forma menos eficaz que [**\_ el método GenerateThumbnail,**](ivmdisplay--generatethumbnail.md) pero se puede usar desde clientes de scripting. La miniatura siempre tiene 64 píxeles de ancho por 48 píxeles de alto. Cada píxel es de 32 bits. Los primeros 64 elementos de la matriz son la primera fila de píxeles de la miniatura, los 64 elementos siguientes son la segunda fila, y así sucesivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

