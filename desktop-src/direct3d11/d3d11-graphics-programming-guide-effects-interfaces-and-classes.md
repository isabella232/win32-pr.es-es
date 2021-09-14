---
title: Interfaces y clases en efectos
description: Hay muchas maneras de usar clases e interfaces en Efectos 11.
ms.assetid: 526d477b-fc1f-4bd0-a620-ce9b78147f68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b067b8e03b2d43ea44ccab6164424cbc84c7237
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361297"
---
# <a name="interfaces-and-classes-in-effects"></a>Interfaces y clases en efectos

Hay muchas maneras de usar clases e interfaces en Efectos 11. Para obtener la sintaxis de interfaz y clase, [vea Interfaces y clases](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).

En las secciones siguientes se detalla cómo especificar instancias de clase para un sombreador que usa interfaces. Usaremos la siguiente interfaz y clases en los ejemplos:


```
interface IColor
{
  float4 GetColor();
};

class CRed : IColor
{
  float4 GetColor() { return float4(1,0,0,1); }
};
class CGreen : IColor
{
  float4 GetColor() { return float4(0,1,0,1); }
};

CRed pRed;
CGreen pGreen;
IColor pIColor;
IColor pIColor2 = pRed;
```



Tenga en cuenta que las instancias de interfaz se pueden inicializar en instancias de clase. También se admiten matrices de instancias de clase e interfaz y se pueden inicializar como en el ejemplo siguiente:


```
CRed pRedArray[2];
IColor pIColor3 = pRedArray[1];
IColor pIColorArray[2] = {pRed, pGreen};
IColor pIColorArray2[2] = pRedArray;
```



## <a name="uniform-interface-parameters"></a>Parámetros uniformes de interfaz

Al igual que otros tipos de datos uniformes, se deben especificar parámetros de interfaz uniformes en la llamada a CompileShader. Los parámetros de interfaz se pueden asignar a instancias de interfaz global o instancias de clase global. Cuando se asigna a una instancia de interfaz global, el sombreador tendrá una dependencia en la instancia de interfaz, lo que significa que debe establecerse en una instancia de clase. Cuando se asigna a instancias de clase global, el compilador especializa el sombreador (como con otros tipos de datos uniformes) para usar esa clase. Esto es importante para dos escenarios:

1.  Los sombreadores con un destino de 4 x pueden usar parámetros de interfaz si estos parámetros son uniformes y se asignan a instancias de clase global (por lo que no se usa \_ vinculación dinámica).
2.  Los usuarios pueden decidir tener muchos sombreadores compilados y especializados sin vinculación dinámica o pocos sombreadores compilados con vinculación dinámica.


```
float4 PSUniform( uniform IColor color ) : SV_Target
{
  return color;
}

technique11
{
  pass
  {
    SetPixelShader( CompileShader( ps_4_0, PSUniform(pRed) ) );
  }
  pass
  {
    SetPixelShader( CompileShader( ps_5_0, PSUniform(pIColor2) ) );
  }
}
```



Si pIColor2 permanece sin cambios a través de la API, los dos pasos anteriores son funcionalmente equivalentes, pero el primero usa un sombreador estático ps 4 0 mientras que el segundo usa un sombreador \_ \_ ps \_ 5 0 con vinculación \_ dinámica. Si se cambia pIColor2 a través de la API de efectos (consulte Configuración de instancias de clase a continuación), el comportamiento del sombreador de píxeles en el segundo paso puede cambiar.

## <a name="non-uniform-interface-parameters"></a>Parámetros de interfaz no uniformes

Los parámetros de interfaz no uniformes crean dependencias de interfaz para los sombreadores. Al aplicar un sombreador con parámetros de interfaz, estos parámetros se deben asignar en con la llamada BindInterfaces. Las instancias de interfaz global y las instancias de clase global se pueden especificar en la llamada a BindInterfaces.


```
float4 PSAbstract( IColor color ) : SV_Target
{
  return color;
}

PixelShader pPSAbstract = CompileShader( ps_5_0, PSAbstract(pRed) );

technique11
{
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pRed ) );
  }
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pIColor2 ) );
  }
}
```



Si pIColor2 permanece sin cambios a través de la API, los dos pasos anteriores son funcionalmente equivalentes y ambos usan vinculación dinámica. Si se cambia pIColor2 a través de la API de efectos (consulte Configuración de instancias de clase a continuación), el comportamiento del sombreador de píxeles en el segundo paso puede cambiar.

## <a name="setting-class-instances"></a>Establecer instancias de clase

Al establecer un sombreador con vinculación de sombreador dinámico al dispositivo Direct3D 11, también se deben especificar instancias de clase. Es un error establecer este tipo de sombreador con una instancia de clase **NULL.** Por lo tanto, todas las instancias de interfaz a las que hace referencia un sombreador deben tener una instancia de clase asociada.

En el ejemplo siguiente se muestra cómo obtener una variable de instancia de clase de un efecto y establecerla en una variable de interfaz:


```
ID3DX11EffectPass* pPass = pEffect->GetTechniqueByIndex(0)->GetPassByIndex(1);

ID3DX11EffectInterfaceVariable* pIface = pEffect->GetVariableByName( "pIColor2" )->AsInterface();
ID3DX11EffectClassInstanceVariable* pCI = pEffect->GetVariableByName( "pGreen" )->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );

// Apply the same pass with a different class instance
pCI = pEffect->GetVariableByName( "pRedArray" )->GetElement(1)->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 