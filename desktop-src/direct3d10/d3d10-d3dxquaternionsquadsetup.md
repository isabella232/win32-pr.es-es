---
description: Configura los puntos de control para la interpolación Quadrangle esférica.
ms.assetid: c66227bd-8cc1-4173-9dc2-5aab9d57301e
title: Función D3DXQuaternionSquadSetup (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4a0683bce3642b0300e68be348d8aed39b3c333d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708027"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx10mathh"></a>Función D3DXQuaternionSquadSetup (D3DX10Math. h)

Configura los puntos de control para la interpolación Quadrangle esférica.

## <a name="syntax"></a>Sintaxis


```C++
void D3DXQuaternionSquadSetup(
  _In_       D3DXQUATERNION *pAOut,
  _In_       D3DXQUATERNION *pBOut,
  _In_       D3DXQUATERNION *pCOut,
  _In_ const D3DXQUATERNION *pQ0,
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2,
  _In_ const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAOut* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntero a sobre.

</dd> <dt>

*pBOut* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntero que va a estar cerca.

</dd> <dt>

*pCOut* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntero a COut.

</dd> <dt>

*pQ0* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntero al punto de control de entrada, q0.

</dd> <dt>

*pQ1* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntero en el punto de control de entrada, Q1.

</dd> <dt>

*pQ2* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntero en el punto de control de entrada, T2.

</dd> <dt>

*pQ3* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntero al punto de control de entrada, Q3.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Ninguno.

## <a name="remarks"></a>Observaciones

Esta función toma cuatro puntos de control, que se proporcionan a las entradas pQ0, pQ1, pQ2 y pQ3. A continuación, la función modifica estos valores para buscar una curva que fluya a lo largo de la ruta más corta. Los valores de q0, T2 y Q3 se calculan como se muestra a continuación.


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



Una vez calculados los nuevos valores Q, los valores de sobre, cerca de y COut se calculan de la siguiente manera:

Sobre = Q1 \* e<sup> \[ -0,25 \ \* (\ LN \[ exp (Q1) \* T2 \] \ + \ LN \[ exp (Q1) \* q0 \] \) \ \] </sup>

Cerca de = T2 \* e<sup> \[ -0,25 \ \* (\ LN \[ exp (T2) \* Q3 \] \ + \ LN \[ exp (T2) \* Q1 \] \) \] \</sup>

COut = T2

> [!Note]  
> LN es el método de API [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) y exp es el método de API [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).

 

Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.

### <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo usar un conjunto de claves de cuaternión (q0, Q1, T2, Q3) para calcular los puntos de Quadrangle internos (A, B, C). Esto garantiza que las tangentes sean continuas entre segmentos adyacentes.


```
      A     B
Q0    Q1    Q2    Q3
```



En el ejemplo de código siguiente se muestra cómo se puede interpolar entre Q1 y T2.


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
> -   C es +/-T2 según el resultado de la función.
> -   QT es el resultado de la función.
>
> El resultado es un giro de 45 grados alrededor del eje z para Time = 0,5.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
