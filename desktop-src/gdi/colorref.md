---
Description: El valor COLORREF se usa para especificar un color RGB.
ms.assetid: b87d3de2-7a13-44ef-8253-c6851a75fa54
title: COLORREF (Windef.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 3e51b2a906af5939a5c7a8753e5fcc4fbcfae64590e62bcb6df1da2c2bd8426d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761898"
---
# <a name="colorref"></a>COLORREF

El valor COLORREF se usa para especificar un color [RGB.](/windows/desktop/api/Wingdi/nf-wingdi-rgb)


```C++
typedef DWORD COLORREF;
typedef DWORD* LPCOLORREF;
```



## <a name="remarks"></a>Comentarios

Al especificar un color [RGB explícito,](/windows/desktop/api/Wingdi/nf-wingdi-rgb) el **valor COLORREF** tiene el formato hexadecimal siguiente:

`0x00bbggrr`

El byte de orden bajo contiene un valor para la intensidad relativa de rojo; el segundo byte contiene un valor para verde; y el tercer byte contiene un valor para blue. El byte de orden superior debe ser cero. El valor máximo de un solo byte es 0xFF.

Para crear un valor de color **COLORREF,** use la [macro RGB.](/windows/desktop/api/Wingdi/nf-wingdi-rgb) Para extraer los valores individuales de los componentes rojo, verde y azul de un valor de color, use las macros [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)y [GetBValue,](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) respectivamente.

## <a name="example"></a>Ejemplo

```cpp
// Color constants.
const COLORREF rgbRed   =  0x000000FF;
const COLORREF rgbGreen =  0x0000FF00;
const COLORREF rgbBlue  =  0x00FF0000;
const COLORREF rgbBlack =  0x00000000;
const COLORREF rgbWhite =  0x00FFFFFF;
```

Ejemplo de [Windows ejemplos clásicos](https://github.com/microsoft/Windows-classic-samples) en GitHub.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                    |
| Encabezado<br/>                   | <dl> <dt>Windef.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Información general sobre colores](colors.md)
</dt> <dt>

[Estructuras de color](color-structures.md)
</dt> <dt>

[GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue)
</dt> <dt>

[GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)
</dt> <dt>

[**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue)
</dt> <dt>

[RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb)
</dt> </dl>

 

 




