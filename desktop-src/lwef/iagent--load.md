---
title: Carga de IAgent
description: Carga de IAgent
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e30a25abb631714384f8349a9d260deade0d6d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995233"
---
# <a name="iagentload"></a>IAgent:: Load

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

Carga un carácter en la colección de [**caracteres**](./iagent.md) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*
</dt> <dd>

Un tipo de datos Variant que debe ser uno de los siguientes:



|            |                                                                       |
|------------|-----------------------------------------------------------------------|
| *filespec* | Ubicación del archivo local del archivo de definición del carácter especificado. |
| *URL*      | Dirección HTTP del archivo de definición del carácter.                 |



 

</dd> <dt>

<span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*
</dt> <dd>

Dirección de una variable que recibe el identificador del carácter.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador de la solicitud de [**carga**](load-method.md) .

</dd> </dl>

Puede cargar caracteres del subdirectorio del agente de Microsoft especificando una ruta de acceso relativa (una que no incluya un carácter de dos puntos o una barra diagonal inicial). Esto agrega un prefijo a la ruta de acceso con el directorio de caracteres del agente (ubicado en el directorio% Windows% \\ MSAgent localizado). También puede usar una dirección relativa para especificar su propio directorio en el directorio chars del agente.

No se puede cargar el mismo carácter (un carácter que tiene el mismo GUID) más de una vez desde una única conexión. Del mismo modo, no puede cargar el carácter predeterminado y otros caracteres al mismo tiempo desde una sola conexión, ya que el carácter predeterminado podría ser el mismo que el otro carácter. Sin embargo, puede crear otra conexión (mediante CoCreateInstance) y cargar el mismo carácter.

El proveedor de datos de Microsoft Agent admite la carga de datos de caracteres almacenados como un solo archivo estructurado (. ACS) con datos de caracteres y de animación juntos, o como datos de caracteres independientes (. ACF) y animación (. ACA). Por lo general, se usa la estructura única. Archivo de ACS para cargar un carácter que está almacenado en una unidad de disco local o en una red y a la que se tiene acceso mediante el protocolo de archivo convencional (como rutas de acceso UNC). Use la independiente. ACF y. Los archivos ACA cuando desea cargar los archivos de animación de forma individual desde un sitio remoto al que se tiene acceso mediante el protocolo HTTP.

Para. Los archivos de ACS, mediante el método [**Load**](load-method.md) , proporcionan acceso a las animaciones de un carácter; una vez cargados, puede utilizar el método [**Play**](play-method.md) para animar el carácter. Para. Archivos ACF, también se usa el método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para cargar datos de animación. El método **Load** no admite la descarga. Archivos de ACS de un sitio HTTP.

Al cargar un carácter, no se muestra automáticamente el carácter. Use el método [**Show**](show-method.md) primero para que el carácter esté visible.

 

 