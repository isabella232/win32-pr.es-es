---
description: Localizar particiones durante la activación
ms.assetid: a5452ed6-ab0f-4d38-bc16-1de6cbf57486
title: Localizar particiones durante la activación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e8912c8277d79c1a20300a1a880644801d0bcb
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104568673"
---
# <a name="locating-partitions-during-activation"></a>Localizar particiones durante la activación

La ubicación de la partición correcta en la que se va a activar un componente depende de lo siguiente:

-   La llamada de función y los parámetros utilizados en el programa que realiza la llamada para activar el componente
-   Si el componente que se va a activar es local o remoto
-   Uso interno de la memoria caché de partición

## <a name="the-calling-program"></a>El programa que realiza la llamada

COM+ selecciona la partición para la activación de componentes en función de cómo el programa de llamada activa el componente.

Hay tres acciones diferentes que COM+ puede llevar a cabo al seleccionar una partición para la activación de componentes. La acción realizada depende de la forma en que el programa de llamada crea instancias del objeto, es decir, si la llamada de función incluye un moniker de partición, que consta de un identificador de partición y un CLSID, o solo incluye un CLSID.

En la tabla siguiente se muestran las distintas acciones que COM+ puede realizar, en orden de prioridad, para buscar una partición.



| Llamada a función                                                  | Parámetro                                                      | Acción COM+                                                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) o **GetObject**<br/> | Moniker de partición (incluye el identificador de partición y el CLSID)<br/> | Usa el ID. de partición especificado en el moniker de la partición.<br/>                                                                                                                           |
| [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)<br/>        | CLSID<br/>                                               | Usa el ID. de partición de la partición predeterminada de la identidad del usuario o el ID. de partición que se agregó al contexto durante una activación de componente anterior en el mismo proceso.<br/> |



 

Las acciones de COM+ enumeradas en la tabla anterior se explican en las secciones siguientes.

## <a name="use-of-partition-monikers"></a>Uso de monikers de partición

Una partición se puede seleccionar explícitamente dentro de una llamada de función mediante el *moniker* de la partición. Se usa un moniker de partición dentro del código para especificar explícitamente la partición del componente activado. Si se usa un moniker de partición para buscar la partición, la activación se produce desde esa partición. Es decir, el ID. de partición incluido en el moniker tiene prioridad sobre la partición predeterminada del usuario o sobre un identificador de partición que existe en el contexto del autor de la llamada.

En el código de C++, la sintaxis para el uso de un moniker de partición es la siguiente:


```C++
HRESULT CoGetObject(
  L"partition:partitionGUID/new:clsid",
  pBindOptions,
  IID_IUnknown,
  (void**)&pIUnknown);
```



En el ejemplo siguiente se muestra un fragmento de código de C++, en el que se usa un moniker de partición como argumento para la función [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) :


```C++
// Create CLSID1 configured in the Production partition.
HRESULT hr = CoGetObject(
  L"partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1",
  pBindOptions, IID_IUnknown, (void**)&pIUnknown);
```



En Visual Basic código, la sintaxis de un moniker de la partición es la siguiente:


```VB
GetObject("partition:partitionGUID/new:CLSID") As Object
```



En el ejemplo siguiente se muestra un fragmento de código de Visual Basic, en el que se usa un moniker de partición como argumento para la función **GetObject** :


```VB
Dim objCLSID1 As Object
Set objCLSID1 = GetObject( _
   "partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1")
```



## <a name="use-of-default-mapping"></a>Uso de la asignación predeterminada

Cuando se usa la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para activar un componente, mediante el CLSID del componente, com+ utiliza la asignación de identidad de usuario predeterminada, que es el conjunto de particiones al que está asignado el usuario dentro de Active Directory. Sin embargo, si el usuario no está asignado a un conjunto de particiones dentro de Active Directory, se selecciona la partición global.

## <a name="use-of-partition-ids-and-object-context"></a>Uso de ID. de partición y contexto del objeto

Una de las cinco propiedades asignadas a una nueva partición es el identificador de la partición. Cuando el programa cliente llama a la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear una instancia de un objeto, el identificador de la partición se agrega al contexto. Es importante usar el ID. de partición del contexto para encontrar la partición, ya que garantiza que, una vez iniciada una cadena de activaciones, el identificador de la partición sigue siendo el mismo, a menos que se cambie explícitamente a través de un moniker de la partición.

Para obtener información adicional sobre cómo localizar particiones durante la activación, vea [componentes y particiones en cola de com+](com--queued-components-and-partitions.md).

## <a name="local-and-remote-activation"></a>Activación local y remota

-   Si el componente al que se llama existe en otro equipo, se calculan las referencias de las propiedades de la partición (incluido el ID. de partición) al otro equipo y el componente se activa desde la partición serializada. Si no se serializó ningún ID. de partición, COM+ utiliza el conjunto de particiones predeterminado asignado a la identidad del usuario en Active Directory.

## <a name="the-partition-cache"></a>La memoria caché de partición

En un entorno de dominio, COM+ usa las asignaciones en Active Directory para encontrar la partición correcta para la activación de componentes. Sin embargo, las búsquedas frecuentes en Active Directory pueden dar lugar a un tráfico de red excesivo. Para minimizar el tráfico de red resultante de búsquedas frecuentes de asignación de conjunto de usuarios a particiones en Active Directory, COM+ utiliza una *memoria caché de particiones*.

La memoria caché de particiones contiene las asignaciones que se realizaron en Active Directory entre las identidades de usuario o las unidades organizativas y sus conjuntos de particiones. Esta memoria caché de particiones se encuentra en el servidor de aplicaciones en el que residen las aplicaciones COM+.

Cuando COM+ necesita determinar la partición predeterminada de un usuario o validar los derechos de acceso de un usuario en una partición, comprueba la caché de particiones localmente para buscar la asignación del usuario, en lugar de comprobar Active Directory de forma remota.

Si se produce un error en la búsqueda en la caché de particiones, COM+ comprueba Active Directory. Si la búsqueda se realiza correctamente en Active Directory, COM+ almacena esa asignación en la memoria caché de la partición. La próxima vez que se realice una búsqueda para esa asignación de usuario a partición, COM+ la encontrará en la memoria caché de la partición.

En la ilustración siguiente se muestra el proceso que usa COM+ para buscar una partición para la activación de componentes.

![Diagrama que muestra un árbol de solución de problemas para el proceso que usa COM+ para buscar una partición para la activación de componentes.](images/5d00eb4e-4572-491c-85e9-33ceed2cd753.png)

El tamaño de la memoria caché y el tiempo de expiración de las entradas de caché se establecen a través de las claves del registro. Para obtener información sobre la configuración de estas claves del registro, vea [crear y configurar particiones com+](creating-and-configuring-com--partitions.md).

> [!Note]  
> Si un equipo servidor está desconectado de la red y se cambia la asignación de usuario a partición mientras el servidor está desconectado, es posible que la memoria caché de particiones contenga una asignación de usuario a partición no actualizada. Esto podría producir un error de activación si la asignación de usuario a partición es el mecanismo que se usa para activar un componente.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Buscar un componente para la activación](locating-a-component-for-activation.md)
</dt> </dl>

 

