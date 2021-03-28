---
title: Sintaxis de grupo de efectos (Direct3D 11)
description: Un grupo de efectos se declara con la sintaxis descrita en esta sección.
ms.assetid: f6695ae5-198f-45bd-853b-8c02fabd0c39
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9221341810990801f1ed07005e0dcb917df42360
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104487186"
---
# <a name="effect-group-syntax-direct3d-11"></a>Sintaxis de grupo de efectos (Direct3D 11)

Un grupo de efectos se declara con la sintaxis descrita en esta sección.


```
fxgroup GroupName  [ <Annotations > ]
{
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
}



```



## <a name="parameters"></a>Parámetros



| Elemento                                                                                                                                                                           | Descripción                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup<br/>                                                                                                         | palabra clave ecesario.<br/>                                                                                                                                                                                                         |
| <span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>GroupName<br/>                                                                       | Obligatorio. Cadena ASCII que identifica de forma única el nombre del grupo de efectos. A diferencia de las técnicas, los grupos deben tener nombres para asegurarse de que las técnicas tienen un identificador único (consulte la sección grupos y técnicas a continuación).<br/> |
| <span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < anotaciones ><br/> | \[en \] opcional. Una o más partes de la información proporcionada por el usuario (metadatos) que el sistema de efectos omite. Para ver la sintaxis, vea sintaxis de anotación (Direct3D 11). <br/>                                                      |
| <span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion<br/>                                           | "Technique10" o "technique11". Las técnicas que usan la funcionalidad nueva en Direct3D 11 (5 \_ 0 sombreadores, BindInterfaces, etc.) deben usar "technique11".<br/>                                                                 |
| <span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>TechniqueName<br/>                                                       | Opcional. Cadena ASCII que identifica de forma única el nombre de la técnica de efecto. <br/>                                                                                                                                    |



 

## <a name="groups-and-techniques"></a>Grupos y técnicas

Para mantener la compatibilidad con efectos de FX \_ 4 \_ 0, los grupos son opcionales. Hay un grupo de nombres NULL implícito que rodea todas las técnicas globales.

Considere el ejemplo siguiente:


```
technique11 GlobalTech
{
}
fxgroup Group1
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
fxgroup Group2
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
```



En C++, se puede obtener una técnica por nombre de dos maneras. Los siguientes comandos encontrarán las técnicas obvias:


```
pEffect->GetTechniqueByName( "GlobalTech" );
pEffect->GetTechniqueByName( "|GlobalTech" );
pEffect->GetTechniqueByName( "Group1|Tech1" );
pEffect->GetTechniqueByName( "Group1|Tech2" );
pEffect->GetTechniqueByName( "Group2|Tech1" );
pEffect->GetTechniqueByName( "Group2|Tech2" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech2" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech2" );
```



Para asegurarse de que [**ID3DX11Effect:: GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) funciona de forma similar a los efectos 10, todos los grupos definidos deben tener un nombre.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](d3d11-effect-format.md)
</dt> <dt>

[Sintaxis de la técnica de efectos (Direct3D 11)](d3d11-effect-technique-syntax.md)
</dt> </dl>

 

 





