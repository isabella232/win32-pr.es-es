---
title: Firmas raíz
description: La firma raíz define qué tipos de recursos están enlazados a la canalización de gráficos.
ms.assetid: ee32a222-8469-4af5-b688-afa70cf77c6a
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4c034e208dd841545777cc92878e7020b9b4a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072878"
---
# <a name="root-signatures"></a>Firmas raíz

La firma raíz define qué tipos de recursos están enlazados a la canalización de gráficos.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introducción a las firmas raíz](root-signatures-overview.md)<br/>                                                 | La aplicación configura una firma raíz y vincula listas de comandos a los recursos que requieren los sombreadores. La lista de comandos de gráficos tiene una firma raíz de gráficos y de proceso. Una lista de comandos de proceso simplemente tendrá una firma raíz de proceso. Estas firmas raíz son independientes entre sí.<br/>                                                                                             |
| [Uso de una firma raíz](using-a-root-signature.md)<br/>                                                     | La firma raíz es la definición de una colección arbitrariamente organizada de tablas de descriptores (incluido su diseño), constantes raíz y descriptores raíz. Cada entrada tiene un costo hacia un límite máximo, por lo que la aplicación puede equilibrar el equilibrio entre el número de cada tipo de entrada que contendrá la firma raíz.<br/>                                                                     |
| [Creación de una firma raíz](creating-a-root-signature.md)<br/>                                               | Las firmas raíz son una estructura de datos compleja que contiene estructuras anidadas. Se pueden definir mediante programación mediante la definición de estructura de datos siguiente (que incluye métodos para ayudar a inicializar miembros). Como alternativa, se pueden crear en lenguaje de sombreado de alto nivel (HLSL), lo que da la ventaja de que el compilador validará pronto que el diseño es compatible con el sombreador. <br/> |
| [Límites de la firma raíz](root-signature-limits.md)<br/>                                                       | La firma raíz es el patrimonio real principal y hay límites y costos estrictos que se deben tener en cuenta.<br/>                                                                                                                                                                                                                                                                                                            |
| [Uso de constantes directamente en la firma raíz](using-constants-directly-in-the-root-signature.md)<br/>     | Las aplicaciones pueden definir constantes raíz en la firma raíz, cada una como un conjunto de valores de 32 bits. Aparecen en lenguaje de sombreado de alto nivel (HLSL) como búfer constante. Tenga en cuenta que los búferes constantes por motivos históricos se ven como conjuntos de valores de 4x32 bits. <br/>                                                                                                                                        |
| [Uso de descriptores directamente en la firma raíz](using-descriptors-directly-in-the-root-signature.md)<br/> | Las aplicaciones pueden colocar descriptores directamente en la firma raíz para evitar tener que pasar por un montón de descriptores. Estos descriptores toman mucho espacio en la firma raíz (consulte la sección límites de firma raíz), por lo que las aplicaciones tienen que usarlas con moderación. <br/>                                                                                                                                     |
| [Ejemplos de firmas raíz](example-root-signatures.md)<br/>                                                   | En la sección siguiente se muestran las firmas raíz que varían en complejidad, de vacías a completamente llenas.<br/>                                                                                                                                                                                                                                                                                                       |
| [Especificación de firmas de raíz en HLSL](specifying-root-signatures-in-hlsl.md)<br/>                             | Especificar firmas raíz en el modelo de sombreador HLSL 5.1 es una alternativa a especificarlas en código de C++.<br/>                                                                                                                                                                                                                                                                                                  |
| [Versión 1.1 de la firma raíz](root-signature-version-1-1.md)<br/>                                             | El propósito de la versión 1.1 de la firma raíz es permitir que las aplicaciones indiquen a los controladores cuándo los descriptores de un montón de descriptores no cambiarán o los descriptores de datos apuntan a que no cambiarán. Esto permite que los controladores realicen optimizaciones que podrían ser posibles sabiendo que un descriptor o la memoria a la que apunta es estático durante un período de tiempo. <br/>                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)
</dt> <dt>

[**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer)
</dt> <dt>

[Enlace de recursos](resource-binding.md)
</dt> </dl>

 

