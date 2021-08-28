---
description: 'Estructura D3DXMATRIXA16 (D3DX10Math.h): matriz alineada en 4x4 y 16 bytes que contiene métodos y sobrecargas de operadores.'
ms.assetid: d9e9c1cc-7555-4011-a4b4-8cce20404841
title: Estructura D3DXMATRIXA16 (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIXA16
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 4953b51cdd09cdbcac4855bd423ce37dda5b979e06153589b5b2ded21004b3ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853405"
---
# <a name="d3dxmatrixa16-structure-d3dx10mathh"></a>Estructura D3DXMATRIXA16 (D3DX10Math.h)

Matriz de 4x4 y 16 bytes alineada que contiene métodos y sobrecargas de operadores.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Ij**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente (i, j) de la matriz, donde i es el número de fila y j es el número de columna. Por ejemplo, 34 significa lo mismo que a₃₄ , el componente de \_ la tercera fila y la cuarta \[ \] columna.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una matriz alineada de 16 bytes, cuando la usan las funciones matemáticas D3DX, se ha optimizado para mejorar el rendimiento en procesadores Intel Pentium 4. Las matrices se alinean independientemente de dónde se creen: en la pila del programa, en el montón o en el ámbito global. La alineación se realiza mediante \_ \_ declspec(align(16)), que funciona con Visual C++ .NET y con Visual C++ 6.0 solo cuando se instala el paquete de procesador. Desafortunadamente, no hay ninguna manera de detectar el paquete de procesador, por lo que la alineación de bytes está activada de forma predeterminada solo con Visual C++ .NET.

Los vectores y cuaterniones no están alineados en bytes en D3DX. Al usar vectores y cuaterniones con funciones matemáticas D3DX, use \_ declspec(align(16)) para generar vectores y cuaterniones alineados con bytes, ya que tendrán un rendimiento considerablemente mejor. La definición \_ de declspec se muestra aquí.


```
#define D3DX_ALIGN16 __declspec(align(16))
```



Otros compiladores **interpretan D3DXMATRIXA16** como [**D3DXMATRIX.**](d3d10-d3dxmatrix.md) El uso de esta estructura en un compilador que no alinea realmente la matriz puede ser problemático porque no expondrá errores que omiten la alineación. Por ejemplo, si un objeto **D3DXMATRIXA16** está dentro de una estructura o clase, se podría realizar [una memcpy](https://msdn2.microsoft.com/library/dswaw1wk(vs.71).aspx) con empaquetado estricto (omitiendo los límites de 16 bytes). Esto provocaría interrupciones de compilación si el compilador agregara alguna vez la alineación de la matriz.

### <a name="d3dxmatrixa16-extensions"></a>Extensiones D3DXMATRIXA16

**D3DXMATRIXA16 tiene** las siguientes extensiones de C++.


```
typedef struct _D3DXMATRIXA16 : public D3DXMATRIX
{
    _D3DXMATRIXA16();
    _D3DXMATRIXA16( CONST FLOAT * f);
    _D3DXMATRIXA16( CONST D3DMATRIX& m);
    _D3DXMATRIXA16( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                    FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                    FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                    FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );
    void* operator new(size_t s);
    void* operator new[](size_t s);

    // The two operators below are not virtual operators. If you cast
    //   to D3DXMATRIX, do not delete using them
    void operator delete(void* p);
    void operator delete[](void* p);

    struct _D3DXMATRIXA16& operator=(CONST D3DXMATRIX& rhs);
} _D3DXMATRIXA16;

typedef D3DX_ALIGN16 _D3DXMATRIXA16 D3DXMATRIXA16, *LPD3DXMATRIXA16;
        
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
