---
title: Almacenar variables y tipos para los sombreadores que se van a compartir
description: El objeto de vinculación de clases es un espacio de nombres para variables y tipos que pueden compartir varios sombreadores.
ms.assetid: 8b61677b-a466-4646-b0b2-19097669f8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f9423154cd42de28b2d447776fe21a7b8e57620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984071"
---
# <a name="storing-variables-and-types-for-shaders-to-share"></a>Almacenar variables y tipos para los sombreadores que se van a compartir

El objeto de vinculación de clases es un espacio de nombres para variables y tipos que pueden compartir varios sombreadores. Cuando se pasa un objeto de vinculación de clase en una llamada a para crear un sombreador, el tiempo de ejecución recopila una lista de variables y tipos que pueden implementar cada interfaz en el sombreador y almacena los nombres de esas variables y tipos en el objeto de vinculación de clases.

Por lo tanto, cuando se llama al método [**ID3D11ClassLinkage:: GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) para generar instancias de clase desde el objeto de vinculación de clase, el runtime puede recuperar la variable o el tipo que se corresponde con el nombre proporcionado en cada sombreador (si ese nombre es válido para un sombreador determinado) y que se crea con el objeto de vinculación de clase especificado.

Por ejemplo, supongamos que tiene una clase **Light** que implementa una interfaz de **color** y usa esta clase en el sombreador de vértices y en el sombreador de píxeles. Al crear un sombreador (por ejemplo, llamando a [**ID3D11Device:: CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)), el tiempo de ejecución determina que el tipo de clase **Light** está disponible en los sombreadores de vértices y píxeles y agrega el tipo de clase **Light** al objeto de vinculación de clase. Después, puede crear una instancia de **Light** en la ubicación que desee, enlazar los recursos de ambos sombreadores y pasar esta instancia en la matriz de instancias de clase al establecer el sombreador en el dispositivo (por ejemplo, mediante una llamada a [**ID3D11DeviceContext::P ssetshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)). A continuación, el tiempo de ejecución realiza la siguiente secuencia:

1.  Comprueba que la instancia de se creó con el mismo objeto de vinculación de clase.
2.  Comprueba que el tipo de clase **Light** está disponible en los sombreadores de vértices y píxeles.
3.  Selecciona las tablas de funciones correctas, que pueden ser diferentes para los sombreadores de vértices y píxeles.
4.  Envía los desplazamientos que proporciona la instancia de.

En última instancia, el objeto de vinculación de clases es un repositorio de nombres de tipo y variable. El número máximo de nombres disponibles para cada elemento (tipo y variable) es de 64 KB. Cuanto más largas sean los nombres de tipo y variable, mayor será el requisito de almacenamiento de los metadatos de la interfaz que se almacenan por cada sombreador. Esto se debe a que el Runtime debe almacenar una asignación para estos nombres para cada sombreador.

## <a name="related-topics"></a>Temas relacionados

[Vinculación dinámica](overviews-direct3d-11-hlsl-dynamic-linking.md)


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vinculación dinámica](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 