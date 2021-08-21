---
description: CPersistStream es la clase base para las propiedades persistentes de los filtros (es decir, filtrar propiedades en gráficos guardados).
ms.assetid: 8073e2be-aaf9-4b01-a7d5-bab5c1dcc19b
title: CPersistStream (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream
api_type:
- COM
api_location: ''
ms.openlocfilehash: 60a48b35ae1559e9b8dfa718c5bca38689cdf0101ce4a343a907b713c8988de0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073589"
---
# <a name="cpersiststream-class"></a>CPersistStream (clase)

![jerarquía de clases cpersiststream](images/pstrm01.png)

`CPersistStream` es la clase base para las propiedades persistentes de los filtros (es decir, filtrar propiedades en gráficos guardados).

La manera más sencilla de `CPersistStream` usar es:

1.  Organice para que el filtro herede esta clase.
2.  Implemente [**WriteToStream**](cpersiststream-writetostream.md) [**y ReadFromStream**](cpersiststream-readfromstream.md) en la clase . Estas invalidarán las funciones aquí, que no hacen nada más que actuar como marcadores de posición.
3.  Cambie **nonDelegatingQueryInterface para** controlar **IPersistStream.**
4.  Implemente [**SizeMax**](cpersiststream-sizemax.md) para devolver un límite superior en el número de bytes de datos guardados.

    Si guarda datos ™ Unicode, recuerde que un WCHAR es de 2 bytes.

5.  Cuando cambien los datos, llame [**a SetDirty**](cpersiststream-setdirty.md).

## <a name="version-numbers"></a>Números de versión

En algún momento puede decidir modificar o ampliar el formato de los datos. A continuación, le gustaría tener un número de versión en todas las secuencias guardadas antiguas para poder saber, al leerlas, si representan el formulario antiguo o nuevo. Para ayudarle, esta clase escribe y lee un número de versión. Cuando escribe, llama a [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) para consultar la versión del software que se usa en este momento. (En efecto, se trata de un número de versión del diseño de datos en el archivo). Escribe esto como lo primero en los datos. Si desea cambiar la versión, implemente (invalide) **GetSoftwareVersion**. Lee el número de versión del archivo en **mPS \_ dwFileVersion** antes de llamar a [**ReadFromStream,**](cpersiststream-readfromstream.md)por lo que en **ReadFromStream** puede comprobar **mPS \_ dwFileVersion** para ver si está leyendo un archivo de versión anterior. Normalmente, debe aceptar archivos cuya versión no sea más reciente que la versión de software que los está leyendo.

**CPersistStream** implementa [**IPersistStream.**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) Para obtener más información sobre la implementación, consulte la Referencia COM en el SDK de la plataforma de Microsoft.



| Miembros de datos protegidos                                          | Descripción                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| mPS \_ dwFileVersion                                              | Número de versión del archivo.                                                   |
| mPS \_ fDirty                                                     | Se deben guardar los datos de esta secuencia.                                           |
| Funciones de miembro                                                | Descripción                                                                   |
| [**CPersistStream**](cpersiststream-cpersiststream.md)         | Construye un **objeto CPersistStream.**                                       |
| [**SetDirty**](cpersiststream-setdirty.md)                     | Indica que el objeto debe guardarse en la secuencia.                        |
| Funciones miembro reemplazables                                    | Descripción                                                                   |
| [**GetClassID**](cpersiststream-getclassid.md)                 | Recupera el identificador de clase de esta secuencia.                                |
| [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) | Recupera el número de versión para este formato de archivo.                            |
| [**ReadFromStream**](cpersiststream-readfromstream.md)         | Lee los datos del filtro de la secuencia.                                      |
| [**SizeMax**](cpersiststream-sizemax.md)                       | Recupera el número de bytes necesarios para los datos (sin incluir el número de versión). |
| [**WriteToStream**](cpersiststream-writetostream.md)           | Escribe los datos del filtro en la secuencia.                                       |
| Métodos IPersistStream                                          | Descripción                                                                   |
| [**GetSizeMax**](cpersiststream-getsizemax.md)                 | Recupera el número de bytes necesarios para los datos (incluido el número de versión).     |
| [**IsDirty**](cpersiststream-isdirty.md)                       | Comprueba si el objeto debe guardarse.                                           |
| [**Cargar**](cpersiststream-load.md)                             | Carga los datos del flujo en memoria.                                   |
| [**Guardar**](cpersiststream-save.md)                             | Guarda los datos de la memoria en la secuencia.                                     |



 

 

 
