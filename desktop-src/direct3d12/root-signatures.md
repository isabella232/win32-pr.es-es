---
title: Firmas raíz
description: La firma raíz define los tipos de recursos que se enlazan a la canalización de gráficos.
ms.assetid: ee32a222-8469-4af5-b688-afa70cf77c6a
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4c034e208dd841545777cc92878e7020b9b4a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549133"
---
# <a name="root-signatures"></a>Firmas raíz

La firma raíz define los tipos de recursos que se enlazan a la canalización de gráficos.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introducción a las firmas raíz](root-signatures-overview.md)<br/>                                                 | La aplicación y los vínculos muestran las listas de comandos a los recursos que requieren los sombreadores. La lista de comandos gráficos tiene un gráfico y una firma de raíz de proceso. Una lista de comandos de proceso simplemente tendrá una firma de raíz de proceso. Estas firmas raíz son independientes entre sí.<br/>                                                                                             |
| [Usar una firma raíz](using-a-root-signature.md)<br/>                                                     | La firma raíz es la definición de una colección de tablas de descriptores organizadas de forma arbitraria (incluido su diseño), constantes raíz y descriptores raíz. Cada entrada tiene un costo hacia un límite máximo, por lo que la aplicación puede desplazarse por el equilibrio entre el número de cada tipo de entrada que contendrá la firma raíz.<br/>                                                                     |
| [Crear una firma raíz](creating-a-root-signature.md)<br/>                                               | Las signaturas raíz son una estructura de datos compleja que contiene estructuras anidadas. Se pueden definir mediante programación usando la definición de la estructura de datos siguiente (que incluye métodos para ayudar a inicializar los miembros). Como alternativa, se pueden crear en el lenguaje de sombreado de alto nivel (HLSL), lo que proporciona la ventaja de que el compilador se validará antes de que el diseño sea compatible con el sombreador. <br/> |
| [Límites de la firma raíz](root-signature-limits.md)<br/>                                                       | La firma raíz es una auténtica inmobiliaria y se deben tener en cuenta los límites y costos estrictos.<br/>                                                                                                                                                                                                                                                                                                            |
| [Usar constantes directamente en la firma raíz](using-constants-directly-in-the-root-signature.md)<br/>     | Las aplicaciones pueden definir constantes raíz en la firma raíz, cada una como un conjunto de valores de 32 bits. Aparecen en el lenguaje de sombreado de alto nivel (HLSL) como un búfer de constantes. Tenga en cuenta que los búferes de constantes para las razones históricas se ven como conjuntos de valores de 4x32 bits. <br/>                                                                                                                                        |
| [Usar descriptores directamente en la firma raíz](using-descriptors-directly-in-the-root-signature.md)<br/> | Las aplicaciones pueden poner descriptores directamente en la firma raíz para evitar tener que pasar por un montón de descriptores. Estos descriptores ocupan mucho espacio en la firma raíz (consulte la sección límites de la firma raíz), por lo que las aplicaciones tienen que usarlos con moderación. <br/>                                                                                                                                     |
| [Firmas raíz de ejemplo](example-root-signatures.md)<br/>                                                   | En la siguiente sección se muestran firmas raíz que varían en complejidad de vacío a completo.<br/>                                                                                                                                                                                                                                                                                                       |
| [Especificación de firmas de raíz en HLSL](specifying-root-signatures-in-hlsl.md)<br/>                             | Especificar firmas raíz en el modelo de sombreador de HLSL 5,1 es una alternativa a especificarlas en código de C++.<br/>                                                                                                                                                                                                                                                                                                  |
| [Versión de firma raíz 1,1](root-signature-version-1-1.md)<br/>                                             | El propósito de la versión 1,1 de la firma raíz es permitir que las aplicaciones indiquen los controladores cuando los descriptores de un montón de descriptores logran cambiar o los descriptores de datos apuntan a un cambio de t. Esto permite que los controladores realicen optimizaciones que podrían ser posibles sabiendo que un descriptor o la memoria a la que apunta es estático durante un período de tiempo. <br/>                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)
</dt> <dt>

[**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer)
</dt> <dt>

[Enlace de recursos](resource-binding.md)
</dt> </dl>

 

