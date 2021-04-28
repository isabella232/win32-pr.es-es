---
description: 'Función D3DXQuaternionSquadSetup (D3dx9math.h): configura puntos de control para la interpolación de cuadrángulo esférico.'
ms.assetid: f800d457-8546-49a1-800e-e5c27af96710
title: Función D3DXQuaternionSquadSetup (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquadSetup
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1dcaa90380ec703b4b56458906ab8bd965d7568c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093953"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx9mathh"></a>Función D3DXQuaternionSquadSetup (D3dx9math.h)

Configura puntos de control para la interpolación de cuadrángulo esférica.

## <a name="syntax"></a>Sintaxis


```C++
void D3DXQuaternionSquadSetup(
  _Out_       D3DXQUATERNION *pAOut,
  _Out_       D3DXQUATERNION *pBOut,
  _Out_       D3DXQUATERNION *pCOut,
  _In_  const D3DXQUATERNION *pQ0,
  _In_  const D3DXQUATERNION *pQ1,
  _In_  const D3DXQUATERNION *pQ2,
  _In_  const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAOut* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a AOut.

</dd> <dt>

*pBOut* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a BOut.

</dd> <dt>

*pCOut* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a COut.

</dd> <dt>

*pQ0* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntero al punto de control de entrada, Q0.

</dd> <dt>

*pQ1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntero al punto de control de entrada, Q1.

</dd> <dt>

*pQ2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntero al punto de control de entrada, Q2.

</dd> <dt>

*pQ3* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntero al punto de control de entrada, Q3.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Ninguno.

## <a name="remarks"></a>Comentarios

Esta función toma cuatro puntos de control, que se proporcionan a las entradas pQ0, pQ1, pQ2 y pQ3. A continuación, la función modifica estos valores para buscar una curva que fluye a lo largo de la ruta de acceso más corta. Los valores de q0, q2 y q3 se calculan como se muestra a continuación.


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



Una vez calculados los nuevos valores de Q, los valores de AOut, BOut y COut se calculan de la siguiente manera:

AOut = q1 \* e<sup> \[ -0.25\ \* (\ Ln \[ Exp(q1) \* q2 \] \ +\ Ln \[ Exp(q1) \* q0 \ \] )\ \] </sup>

BOut = q2 \* e<sup> \[ -0.25\ \* (\ Ln \[ Exp(q2) \* q3 \] \ +\ Ln \[ Exp(q2) \* q1 \ \] )\ \] </sup>

COut = q2

> [!Note]  
> Ln es el método de API [**D3DXQuaternionLn**](d3dxquaternionln.md) y Exp es el método de API [**D3DXQuaternionExp**](d3dxquaternionexp.md).

 

Use [**D3DXQuaternionNormalize para cualquier**](d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.

### <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo usar un conjunto de claves de cuaternión (Q0, Q1, Q2, Q3) para calcular los puntos de cuadrángulo internos (A, B, C). Esto garantiza que las tangentes son continuas en segmentos adyacentes.


```
      A     B
Q0    Q1    Q2    Q3
```



En el ejemplo de código siguiente se muestra cómo puede interpolar entre Q1 y Q2.


```
// Rotation about the z-axis
D3DXQUATERNION Q0 = D3DXQUATERNION(0,  0, 0.707f, -.707f);
D3DXQUATERNION Q1 = D3DXQUATERNION(0,  0, 0.000f, 1.000f);
D3DXQUATERNION Q2 = D3DXQUATERNION(0,  0, 0.707f, 0.707f);
D3DXQUATERNION Q3 = D3DXQUATERNION(0,  0, 1.000f, 0.000f);
D3DXQUATERNION A, B, C, Qt;
FLOAT time = 0.5f;

D3DXQuaternionSquadSetup(&A, &B, &C, &Q0, &Q1, &Q2, &Q3);
D3DXQuaternionSquad(&Qt, &Q1, &A, &B, &C, time);
```



> [!Note]
>
> -   C es +/- Q2 en función del resultado de la función.
> -   Qt es el resultado de la función.
>
> El resultado es una rotación de 45 grados alrededor del eje Z para el tiempo = 0,5.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionSquad**](d3dxquaternionsquad.md)
</dt> </dl>

 

 




