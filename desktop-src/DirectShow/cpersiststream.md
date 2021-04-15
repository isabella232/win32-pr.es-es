---
description: CPersistStream es la clase base para las propiedades persistentes de los filtros (es decir, las propiedades de filtro en los gráficos guardados).
ms.assetid: 8073e2be-aaf9-4b01-a7d5-bab5c1dcc19b
title: Clase CPersistStream
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
ms.openlocfilehash: 690a0f45fab7c3612d215a859798460abc81728e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536741"
---
# <a name="cpersiststream-class"></a>Clase CPersistStream

![jerarquía de clases cpersiststream](images/pstrm01.png)

`CPersistStream` es la clase base para las propiedades persistentes de los filtros (es decir, las propiedades de filtro en los gráficos guardados).

La manera más sencilla de usar `CPersistStream` es:

1.  Organice para que el filtro herede esta clase.
2.  Implemente [**WriteToStream**](cpersiststream-writetostream.md) y [**ReadFromStream**](cpersiststream-readfromstream.md) en la clase. Estos invalidarán las funciones aquí, que no hacen nada pero actúan como marcadores de posición.
3.  Cambie **NonDelegatingQueryInterface** para controlar **IPersistStream**.
4.  Implemente [**SizeMax**](cpersiststream-sizemax.md) para devolver un límite superior en el número de bytes de datos que se guardan.

    Si guarda datos de™ Unicode, recuerde que WCHAR tiene 2 bytes.

5.  Cuando cambien los datos, llame a [**SetDirty**](cpersiststream-setdirty.md).

## <a name="version-numbers"></a>Números de versión

En algún momento puede decidir modificar o ampliar el formato de los datos. A continuación, le interesará tener un número de versión en todas las secuencias guardadas antiguas para que pueda saber cuándo las Lee, si representan el formulario antiguo o nuevo. Para ayudarle, esta clase escribe y lee un número de versión. Cuando escribe, llama a [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) para consultar la versión del software que se usa en ese momento. (En efecto, se trata de un número de versión del diseño de datos en el archivo). Escribe esto como la primera cosa en los datos. Si desea cambiar la versión, implemente (invalide) **GetSoftwareVersion**. Lee el número de versión del archivo en **MP \_ dwFileVersion** antes de llamar a [**ReadFromStream**](cpersiststream-readfromstream.md), por lo que en **ReadFromStream** puede comprobar **MPS \_ dwFileVersion** para ver si está leyendo un archivo de versión anterior. Normalmente, debe aceptar archivos cuya versión no sea más reciente que la versión de software que los Lee.

**CPersistStream** implementa [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream). Para obtener más información sobre la implementación, vea la referencia de COM en el SDK de la plataforma de Microsoft.



| Miembros de datos protegidos                                          | Descripción                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| dwFileVersion de mPS \_                                              | Número de versión del archivo.                                                   |
| fDirty de mPS \_                                                     | Los datos de esta secuencia se deben guardar.                                           |
| Funciones de miembro                                                | Descripción                                                                   |
| [**CPersistStream**](cpersiststream-cpersiststream.md)         | Construye un objeto **CPersistStream** .                                       |
| [**SetDirty**](cpersiststream-setdirty.md)                     | Indica que el objeto se debe guardar en la secuencia.                        |
| Funciones miembro reemplazables                                    | Descripción                                                                   |
| [**GetClassID**](cpersiststream-getclassid.md)                 | Recupera el identificador de clase de esta secuencia.                                |
| [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) | Recupera el número de versión de este formato de archivo.                            |
| [**ReadFromStream**](cpersiststream-readfromstream.md)         | Lee los datos del filtro de la secuencia.                                      |
| [**SizeMax**](cpersiststream-sizemax.md)                       | Recupera el número de bytes necesarios para los datos (sin incluir el número de versión). |
| [**WriteToStream**](cpersiststream-writetostream.md)           | Escribe los datos del filtro en la secuencia.                                       |
| Métodos IPersistStream                                          | Descripción                                                                   |
| [**GetSizeMax**](cpersiststream-getsizemax.md)                 | Recupera el número de bytes necesarios para los datos (incluido el número de versión).     |
| [**IsDirty**](cpersiststream-isdirty.md)                       | Comprueba si se debe guardar el objeto.                                           |
| [**Cargar**](cpersiststream-load.md)                             | Carga los datos de la secuencia en la memoria.                                   |
| [**Guardar**](cpersiststream-save.md)                             | Guarda los datos de la memoria en la secuencia.                                     |



 

 

 
