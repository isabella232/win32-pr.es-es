---
description: Matriz de 4x4, de 16 bytes alineada que contiene métodos y sobrecargas de operador.
ms.assetid: d9e9c1cc-7555-4011-a4b4-8cce20404841
title: Estructura D3DXMATRIXA16 (D3DX10Math. h)
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
ms.openlocfilehash: a33b5efa0e5e714c0b161fed8191702066a44b01
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280472"
---
# <a name="d3dxmatrixa16-structure-d3dx10mathh"></a>Estructura D3DXMATRIXA16 (D3DX10Math. h)

Matriz de 4x4, de 16 bytes alineada que contiene métodos y sobrecargas de operador.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_ij**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

El componente (i, j) de la matriz, donde i es el número de fila y j es el número de columna. Por ejemplo, \_ 34 significa lo mismo que \[ ₃ ₄ \] , el componente de la tercera fila y la cuarta columna.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una matriz alineada de 16 bytes, cuando se usa en las funciones matemáticas de D3DX, se ha optimizado para mejorar el rendimiento de los procesadores Intel Pentium 4. Las matrices se alinean independientemente de dónde se crean: en la pila del programa, en el montón o en el ámbito global. La alineación se logra mediante \_ \_ declspec (Align (16)), que funciona con Visual C++ .net y con Visual C++ 6,0 solo cuando se instala el paquete de procesadores. Desafortunadamente, no hay ninguna manera de detectar el paquete de procesadores, por lo que la alineación de bytes está activada de forma predeterminada solo con Visual C++ .NET.

Los vectores y cuaterniones no están alineados en bytes en D3DX. Al usar vectores y cuaterniones con funciones matemáticas de D3DX, use \_ declspec (Align (16)) para generar vectores alineados de bytes y cuaterniones, ya que se realizarán de forma mucho mejor. \_Aquí se muestra la definición de declspec.


```
#define D3DX_ALIGN16 __declspec(align(16))
```



Otros compiladores interpretan **D3DXMATRIXA16** como [**D3DXMATRIX**](d3d10-d3dxmatrix.md). El uso de esta estructura en un compilador que no alinee realmente la matriz puede ser problemático, ya que no expondrá errores que omitan la alineación. Por ejemplo, si un objeto **D3DXMATRIXA16** está dentro de una estructura o una clase, se puede hacer un [memcpy](https://msdn2.microsoft.com/library/dswaw1wk(vs.71).aspx) con un empaquetado estrecho (omitiendo los límites de 16 bytes). Esto provocaría saltos de compilación si el compilador estuviera en algún momento agregar alineación de matriz.

### <a name="d3dxmatrixa16-extensions"></a>Extensiones de D3DXMATRIXA16

**D3DXMATRIXA16** tiene las siguientes extensiones de C++.


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
| Encabezado<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
