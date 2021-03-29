---
title: Información general del código
description: La siguiente ilustración es una representación conceptual de los bloques de código necesarios para implementar el componente de proveedor de ejemplo de ADSI.
ms.assetid: b353c2d9-ef86-4e4c-ac00-4756fc9ec57d
ms.tgt_platform: multiple
keywords:
- Información general del código AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99a4974ac97488fc051ea80dbde7a8a83fa329e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078372"
---
# <a name="code-overview"></a>Información general del código

La siguiente ilustración es una representación conceptual de los bloques de código necesarios para implementar el componente de proveedor de ejemplo de ADSI. Cada sección se describe en la ilustración siguiente. Los programadores de COM experimentados pueden encontrar que se trata de una información general adecuada del componente de proveedor de ejemplo. Para obtener más información, vea [detalles del código](code-details.md).

![implementación del proveedor de ejemplo](images/dssmco.png)

Los elementos numerados siguientes corresponden a los elementos de bloque de la ilustración.

1.  Cargar el archivo DLL (LibMain. cpp, GUID. cpp). El punto de entrada del archivo DLL. Definiciones de objetos estáticos de generador de clases para los dos objetos de proveedor: GUID. cpp contiene las definiciones de CLSID para las implementaciones de los diversos objetos de componente de proveedor de ejemplo.
2.  Código de creación y generador de clases de objetos de proveedor (Cprovcf. cpp, Cprov. cpp, STDFact. cpp). El objeto de proveedor es el objeto que admite [**IParseDisplayName**](/windows/win32/api/oleidl/nn-oleidl-iparsedisplayname) durante las operaciones de enlace de moniker, como se describe en buscar y enlazar en el componente de proveedor de ejemplo.
3.  Enlazar a un objeto (Getobj. cpp). Este código llama al analizador para comprobar que el ADsPath dado es sintácticamente correcto y, a continuación, realiza cualquier asignación necesaria desde ADsPath a la ruta de acceso del servicio de directorio nativo para el elemento que se va a crear como un objeto Active Directory. Busca la definición de esquema para este tipo de objeto y rellena las propiedades obligatorias. Después de crear el objeto de Active Directory, se recupera un puntero de interfaz a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para el autor de la llamada.
4.  Analizador del espacio de nombres del proveedor (Parse. cpp). Este es el código invocado por el elemento 3. El analizador comprueba que la cadena ADsPath pasada es sintácticamente correcta para su propio espacio de nombres.
5.  Generador de clases, creación y enumeración para el objeto de espacio de nombres (Cnamcf. cpp, Cnamesp. cpp, Cenumns. cpp). El objeto de espacio de nombres es un objeto contenedor que se puede enumerar para buscar todos los objetos de nodo raíz de este espacio de nombres.
6.  Generador de clases y código de creación para un objeto de Active Directory genérico, y el generador de clases, el código de creación y enumeración para un objeto contenedor ADs genérico (Cgenobj. cpp, Cenumobj. cpp, Common. cpp, Core. cpp). Este código se ejecuta cuando se crea un objeto de Active Directory.
7.  Filtrar y enumerar variantes (Cenumvar. cpp, Object. cpp). Cuando una colección de elementos VARIANT de un solo tipo se administra en ADSI, se usa este código.
8.  GLOBALS (Globals. cpp). Palabras clave de espacio de nombres, las estructuras de asignación de sintaxis de formatos de datos nativos al tipo de variante de automatización ADs se definen aquí.
9.  Serialización/desserialización de datos (Pack. cpp, Property. cpp, Smpoper. cpp). La conversión de formatos de datos nativos al conjunto compatible de tipos de variante de automatización se produce cuando las propiedades de un objeto se cargan en la memoria caché de propiedades. Se debe realizar otro control especial para los datos cuando las estructuras con punteros se copian, se eliminan o se mueven en memoria.
10. Caché de propiedades (Cprops. cpp). Propiedades de almacenamiento en caché es una característica del entorno ADSI. Los métodos [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo), [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex)y [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) actúan en la caché de propiedades.
11. Administración de memoria (Memory. cpp). El uso de un conjunto de funciones de memoria para asignar y liberar memoria permite al componente de proveedor de ejemplo realizar un seguimiento del uso de la memoria y detener las pérdidas de memoria.
12. Objetos de esquema y administración (Cschobj. cpp, Cprpobj. cpp, Cclsobj. cpp, Cenumsch. cpp). Esto incluye rutinas para crear, administrar y enumerar los objetos de esquema. Esto incluye objetos de clase de esquema, objetos de propiedad y objetos de sintaxis, además de poder enumerar el objeto contenedor de clase de esquema.
13. Llamadas específicas del sistema operativo (RegDSAPI. cpp). Esto incluye todas las llamadas que hacen referencia al sistema operativo nativo. Entre otras funciones, incluyen funciones de apertura, cierre, lectura y modificación de objetos, así como de los que tienen acceso al esquema y a los datos de propiedades. El componente de proveedor de ejemplo se produjo para simular una jerarquía de directorios mediante el registro. Solo los nombres de función deben ser de gran interés para un escritor de proveedores.
14. Implementación de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (Cdispmgr. cpp). Este código tiene acceso a los datos de la biblioteca de tipos para permitir que se invoquen los métodos de interfaz de una manera compatible con la automatización.

 

 