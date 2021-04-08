---
title: Propiedad IVMDisplay Thumbnail (VPCCOMInterfaces. h)
description: Recupera una matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual. | Propiedad IVMDisplay Thumbnail (VPCCOMInterfaces. h)
ms.assetid: e7b57f16-eec1-4461-acfb-742976eff14a
keywords:
- Propiedad thumbnail Virtual PC
- Propiedad thumbnail Virtual PC, interfaz IVMDisplay
- Interfaz IVMDisplay Virtual PC, propiedad thumbnail
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
ms.openlocfilehash: 0466af2552fbb108f31de94b3f970d6e7d5571b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003499"
---
# <a name="ivmdisplaythumbnail-property"></a>IVMDisplay:: Thumbnail (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera una matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Thumbnail(
  [out, retval] VARIANT *thumbnailImage
);
```



## <a name="property-value"></a>Valor de propiedad

Una variante de tipo VT de \_ matriz VT \| \_ que contiene entradas de tipo VT \_ UI4, una para cada píxel de la miniatura.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **null**.<br/>        |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



## <a name="remarks"></a>Observaciones

Esta interfaz devuelve la miniatura menos eficaz que el método [**\_ GenerateThumbnail**](ivmdisplay--generatethumbnail.md) , pero se puede usar desde los clientes de scripting. La miniatura es siempre de 64 píxeles de ancho por 48 píxeles de alto. Cada píxel es 32 bits. Los primeros 64 elementos de la matriz son la primera fila de píxeles de la miniatura, los siguientes 64 elementos son la segunda fila, etc.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay se define como 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

