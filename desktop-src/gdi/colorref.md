---
Description: El valor COLORREF se usa para especificar un color RGB.
ms.assetid: b87d3de2-7a13-44ef-8253-c6851a75fa54
title: COLORREF (Windef.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 6836cfcc1b18d0b20d5e347fb83206551b27de06
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575029"
---
# <a name="colorref"></a>COLORREF

El valor COLORREF se usa para especificar un color [RGB.](/windows/desktop/api/Wingdi/nf-wingdi-rgb)


```C++
typedef DWORD COLORREF;
typedef DWORD* LPCOLORREF;
```



## <a name="remarks"></a>Observaciones

Al especificar un color [RGB explícito,](/windows/desktop/api/Wingdi/nf-wingdi-rgb) el **valor COLORREF** tiene el formato hexadecimal siguiente:

`0x00bbggrr`

El byte de orden bajo contiene un valor para la intensidad relativa de rojo; el segundo byte contiene un valor para verde; y el tercer byte contiene un valor para azul. El byte de orden superior debe ser cero. El valor máximo de un solo byte es 0xFF.

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



| Requisito | Value |
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

 

 




