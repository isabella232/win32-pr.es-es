---
title: Carga de IAgent
description: Carga de IAgent
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae718ee8c6566de42645c5c02c2efada90ef85ba0136a112bcf0420d18a7b511
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725404"
---
# <a name="iagentload"></a>IAgent::Load

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

Carga un carácter en la [**colección**](./iagent.md) Characters.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*
</dt> <dd>

Tipo de datos variant que debe ser uno de los siguientes:



| Value           | Descripción                                                                      |
|------------|-----------------------------------------------------------------------|
| *Especarchivo* | Ubicación del archivo local del archivo de definición del carácter especificado. |
| *URL*      | Dirección HTTP del archivo de definición del carácter.                 |



 

</dd> <dt>

<span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*
</dt> <dd>

Dirección de una variable que recibe el identificador del carácter.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el [**identificador de solicitud**](load-method.md) de carga.

</dd> </dl>

Puede cargar caracteres desde el subdirectorio de Microsoft Agent especificando una ruta de acceso relativa (una que no incluya dos puntos ni un carácter de barra diagonal inicial). Esto prefida la ruta de acceso con el directorio de caracteres del Agente (ubicado en el directorio %windows% \\ msagent localizado). También puede usar una dirección relativa para especificar su propio directorio en el directorio Chars del agente.

No se puede cargar el mismo carácter (un carácter con el mismo GUID) más de una vez desde una sola conexión. Del mismo modo, no puede cargar el carácter predeterminado y otros caracteres al mismo tiempo desde una sola conexión, porque el carácter predeterminado podría ser el mismo que el otro carácter. Sin embargo, puede crear otra conexión (mediante CoCreateInstance) y cargar el mismo carácter.

El proveedor de datos de Microsoft Agent admite la carga de datos de caracteres almacenados como un único archivo estructurado (. ACS) con datos de caracteres y datos de animación juntos, o como datos de caracteres independientes (. ACF) y animación (. ACA). Por lo general, use la estructura única . Archivo de ACS para cargar un carácter que se almacena en una unidad de disco local o red y al que se accede mediante el protocolo de archivo convencional (por ejemplo, unC pathnames). Use el independiente . ACF y . Archivos ACA cuando quiera cargar los archivos de animación individualmente desde un sitio remoto al que se accede mediante el protocolo HTTP.

Para. Los archivos de ACS, mediante [**el método Load**](load-method.md) proporcionan acceso a las animaciones de un carácter; Una vez cargado, puede usar el [**método Play**](play-method.md) para animar el carácter. Para. Archivos ACF, también se usa el [**método Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para cargar datos de animación. El **método Load** no admite la descarga de . Archivos de ACS desde un sitio HTTP.

La carga de un carácter no muestra automáticamente el carácter. Use primero [**el método Show**](show-method.md) para que el carácter sea visible.

 

 