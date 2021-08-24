---
title: Almacenar variables y tipos para que los sombreadores los compartan
description: El objeto de vinculación de clase es un espacio de nombres para variables y tipos que pueden compartir varios sombreadores.
ms.assetid: 8b61677b-a466-4646-b0b2-19097669f8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d40526274ea52d68b0a02dbefd02c116ded77d64e8b343a48abef2735446d971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853175"
---
# <a name="storing-variables-and-types-for-shaders-to-share"></a>Almacenar variables y tipos para que los sombreadores los compartan

El objeto de vinculación de clase es un espacio de nombres para variables y tipos que pueden compartir varios sombreadores. Cuando se pasa un objeto de vinculación de clase en una llamada para crear un sombreador, el tiempo de ejecución recopila una lista de variables y tipos que pueden implementar cada interfaz en el sombreador y almacena los nombres de esas variables y tipos en el objeto de vinculación de clase.

Por lo tanto, cuando se llama al método [**ID3D11ClassLinkage::GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) para generar instancias de clase a partir del objeto de vinculación de clase, el tiempo de ejecución puede recuperar la variable o el tipo correspondiente al nombre que se proporciona en cada sombreador (si ese nombre es válido para un sombreador determinado) y que se crea con el objeto de vinculación de clase especificado.

Por ejemplo, supongamos que tiene una **clase Light** que implementa una interfaz **Color** y usa esta clase en el sombreador de vértices y el sombreador de píxeles. Al crear un sombreador (por ejemplo, llamando a [**ID3D11Device::CreatePixelShader),**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)el tiempo de ejecución determina que el tipo de clase **Light** está disponible en los sombreadores de vértices y píxeles y agrega el tipo de clase **Light** al objeto de vinculación de clase. A continuación, puede crear una instancia de **Light** en la ubicación que desee, enlazar los recursos de ambos sombreadores y pasar esta instancia en la matriz de instancias de clase al establecer el sombreador en el dispositivo (por ejemplo, llamando a [**ID3D11DeviceContext::P SSetShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)). A continuación, el tiempo de ejecución realiza la siguiente secuencia:

1.  Comprueba que la instancia se creó con el mismo objeto de vinculación de clase.
2.  Comprueba que el tipo **de clase Light** está disponible en los sombreadores de vértices y píxeles.
3.  Selecciona las tablas de funciones correctas, que pueden ser diferentes para los sombreadores de vértices y píxeles.
4.  Envía los desplazamientos que proporciona la instancia.

El objeto de vinculación de clase es en última instancia un repositorio de nombres de tipo y variable. El número máximo de nombres disponibles para cada elemento (tipo y variable) es de 64 K. Cuanto más largos sean los nombres de tipo y variable, mayor será el requisito de almacenamiento para los metadatos de interfaz que se almacenan por sombreador. Esto se debe a que el tiempo de ejecución debe almacenar una asignación para estos nombres para cada sombreador.

## <a name="related-topics"></a>Temas relacionados

[Vinculación dinámica](overviews-direct3d-11-hlsl-dynamic-linking.md)


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vinculación dinámica](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 