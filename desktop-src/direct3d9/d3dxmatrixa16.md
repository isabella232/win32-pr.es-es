---
description: 'Estructura D3DXMATRIXA16 (D3dx9math.h): matriz alineada en 4x4 y 16 bytes que contiene métodos y sobrecargas de operadores.'
ms.assetid: c7082fe5-f98b-4ab7-b8c2-7cdbab4848ad
title: Estructura D3DXMATRIXA16 (D3dx9math.h)
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
- d3dx9math.h
ms.openlocfilehash: 7bb14f23d041ec2634b9710d5620382d8b93da2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094213"
---
# <a name="d3dxmatrixa16-structure-d3dx9mathh"></a>Estructura D3DXMATRIXA16 (D3dx9math.h)

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

Los vectores y cuaterniones no están alineados en bytes en D3DX. Al usar vectores y cuaterniones con funciones matemáticas D3DX, use declspec(align(16)) para generar vectores y cuaterniones alineados con bytes, ya que tendrán un rendimiento considerablemente \_ mejor. La definición \_ de declspec se muestra aquí.


```
#define D3DX_ALIGN16 __declspec(align(16))
```



Otros compiladores interpretan D3DXMATRIXA16 como D3DXMATRIX. El uso de esta estructura en un compilador que no alinea realmente la matriz puede ser problemático porque no expondrá errores que omiten la alineación. Por ejemplo, si un objeto D3DXMATRIXA16 está dentro de una estructura o clase, se podría realizar [**una memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) con empaquetado estricto (omitiendo los límites de 16 bytes). Esto provocaría interrupciones de compilación si el compilador agregara alguna vez la alineación de la matriz.

### <a name="d3dxmatrixa16"></a>D3DXMATRIXA16

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
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXMATRIX**](d3dxmatrix.md)
</dt> </dl>

 

 
