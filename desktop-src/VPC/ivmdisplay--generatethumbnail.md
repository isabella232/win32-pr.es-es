---
title: Método _GenerateThumbnail IVMDisplay (VPCCOMInterfaces. h)
description: Recupera una matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual. | Método _GenerateThumbnail IVMDisplay (VPCCOMInterfaces. h)
ms.assetid: c97bb0ff-55cd-491f-a706-0ba15c9a6b54
keywords:
- _GenerateThumbnail método virtual PC
- Método _GenerateThumbnail Virtual PC, interfaz IVMDisplay
- Interfaz IVMDisplay Virtual PC, método _GenerateThumbnail
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
ms.openlocfilehash: 4084549de96330761bca4f4ec6da65ca150c96e5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105653203"
---
# <a name="ivmdisplay_generatethumbnail-method"></a>IVMDisplay:: \_ GenerateThumbnail (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera una matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT _GenerateThumbnail(
  [out] unsigned long thumbnailImage[3072]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*thumbnailImage* \[ enuncia\]
</dt> <dd>

Matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                 | Descripción                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **null**.<br/>        |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta interfaz devuelve la miniatura de forma más eficaz que la propiedad [**thumbnail**](ivmdisplay-thumbnail.md) , pero no se puede usar desde los clientes de scripting. La miniatura es siempre de 64 píxeles de ancho por 48 píxeles de alto. Cada píxel es 32 bits, donde los 8 bits superiores representan el valor azul del píxel, los 8 bits siguientes representan el valor verde del píxel y los 8 bits siguientes representan el valor rojo del píxel. Los primeros 64 elementos de la matriz son la primera fila de la miniatura, los siguientes 64 elementos son la segunda fila, etc. Este método devuelve una matriz estática de píxeles, que es más eficaz que devolver una **SAFEARRAY** de valores **Variant** , pero no es compatible con los clientes de scripting.

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

 

