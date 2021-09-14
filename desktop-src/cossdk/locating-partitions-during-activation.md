---
description: Buscar particiones durante la activación
ms.assetid: a5452ed6-ab0f-4d38-bc16-1de6cbf57486
title: Buscar particiones durante la activación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e8912c8277d79c1a20300a1a880644801d0bcb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361680"
---
# <a name="locating-partitions-during-activation"></a>Buscar particiones durante la activación

La búsqueda de la partición correcta en la que se va a activar un componente depende de lo siguiente:

-   La llamada de función y los parámetros utilizados en el programa de llamada para activar el componente
-   Si el componente que se activa es local o remoto
-   Uso interno de la caché de particiones

## <a name="the-calling-program"></a>El programa que realiza la llamada

COM+ selecciona la partición para la activación de componentes en función de cómo el programa de llamada activa el componente.

Hay tres acciones diferentes que COM+ puede realizar al seleccionar una partición para la activación de componentes. La acción realizada depende de cómo el programa de llamada crea instancias del objeto, es decir, si la llamada de función incluye un moniker de partición, que consta de un identificador de partición y un CLSID, o incluye solo un CLSID.

En la tabla siguiente se muestran las diversas acciones que COM+ puede realizar, en orden de prioridad, para buscar una partición.



| Llamada a función                                                  | Parámetro                                                      | Acción com+                                                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) o **GetObject**<br/> | Moniker de partición (incluye id. de partición y CLSID)<br/> | Usa el identificador de partición especificado en el moniker de partición.<br/>                                                                                                                           |
| [**Cocreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)<br/>        | CLSID<br/>                                               | Usa el identificador de partición de la partición predeterminada de la identidad de usuario o el identificador de partición que se agregó al contexto durante una activación del componente anterior en el mismo proceso.<br/> |



 

Las acciones com+ enumeradas en la tabla anterior se explican en las secciones siguientes.

## <a name="use-of-partition-monikers"></a>Uso de monikers de partición

Una partición se puede seleccionar explícitamente dentro de una llamada de función mediante un *moniker de partición*. Un moniker de partición se usa dentro del código para especificar explícitamente la partición del componente activado. Si se usa un moniker de partición para localizar la partición, la activación se produce desde esa partición. Es decir, el identificador de partición incluido en el moniker tiene prioridad sobre la partición predeterminada del usuario o sobre un identificador de partición que existe en el contexto del autor de la llamada.

En el código de C++, la sintaxis para el uso de un moniker de partición es la siguiente:


```C++
HRESULT CoGetObject(
  L"partition:partitionGUID/new:clsid",
  pBindOptions,
  IID_IUnknown,
  (void**)&pIUnknown);
```



En el ejemplo siguiente se muestra un fragmento de código de C++, en el que se usa un moniker de partición como argumento para la [**función CoGetObject:**](/windows/desktop/api/objbase/nf-objbase-cogetobject)


```C++
// Create CLSID1 configured in the Production partition.
HRESULT hr = CoGetObject(
  L"partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1",
  pBindOptions, IID_IUnknown, (void**)&pIUnknown);
```



En Visual Basic código, la sintaxis de un moniker de partición es la siguiente:


```VB
GetObject("partition:partitionGUID/new:CLSID") As Object
```



En el ejemplo siguiente se muestra un fragmento de código Visual Basic, en el que se usa un moniker de partición como argumento para la **función GetObject:**


```VB
Dim objCLSID1 As Object
Set objCLSID1 = GetObject( _
   "partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1")
```



## <a name="use-of-default-mapping"></a>Uso de asignación predeterminada

Cuando se usa la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para activar un componente, mediante el CLSID del componente, COM+ usa la asignación predeterminada de identidad de usuario, es decir, el conjunto de particiones al que el usuario está asignado dentro de Active Directory. Sin embargo, si el usuario no está asignado a un conjunto de particiones Active Directory, se selecciona la partición global.

## <a name="use-of-partition-ids-and-object-context"></a>Uso de los iDs de partición y el contexto de objeto

Una de las cinco propiedades asignadas a una nueva partición es el identificador de partición. Cuando el programa cliente llama a la [**función CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear una instancia de un objeto, el identificador de partición se agrega al contexto. El uso del identificador de partición del contexto para localizar la partición es importante porque garantiza que, una vez iniciada una cadena de activaciones, el identificador de partición siga siendo el mismo a menos que se cambie explícitamente a través de un moniker de partición.

Para obtener información adicional sobre cómo buscar particiones durante la activación, vea [Componentes y particiones en cola de COM+.](com--queued-components-and-partitions.md)

## <a name="local-and-remote-activation"></a>Activación local y remota

-   Si el componente al que se llama existe en otro equipo, las propiedades de partición (incluido el identificador de partición) se serializan en el otro equipo y el componente se activa desde la partición serializada. Si no se ha serializado ningún identificador de partición, COM+ usa el conjunto de particiones predeterminado asignado a la identidad del usuario dentro Active Directory.

## <a name="the-partition-cache"></a>La caché de particiones

En un entorno de dominio, COM+ usa las asignaciones de Active Directory para buscar la partición correcta para la activación de componentes. Sin embargo, las búsquedas frecuentes en Active Directory pueden dar lugar a un tráfico de red excesivo. Para minimizar el tráfico de red resultante de búsquedas frecuentes de asignación de usuario a conjunto de particiones en Active Directory, COM+ usa una caché *de particiones*.

La caché de particiones contiene las asignaciones que se realizaron en Active Directory identidades de usuario o U y sus conjuntos de particiones. Esta caché de particiones se encuentra en el servidor de aplicaciones en el que residen las aplicaciones COM+.

Cuando COM+ necesita determinar la partición predeterminada de un usuario o validar los derechos de acceso de un usuario a una partición, comprueba la caché de particiones localmente para buscar la asignación del usuario, en lugar de comprobar Active Directory de forma remota.

Si se produce un error en la búsqueda en la caché de particiones, COM+ comprueba Active Directory. Si la búsqueda se realiza correctamente Active Directory, COM+ almacena esa asignación en la caché de particiones. La próxima vez que se realiza una búsqueda para esa asignación de usuario a partición, COM+ la encontrará en la caché de particiones.

En la ilustración siguiente se muestra el proceso que COM+ usa para buscar una partición para la activación de componentes.

![Diagrama que muestra un árbol de solución de problemas para el proceso que COM+ usa para buscar una partición para la activación de componentes.](images/5d00eb4e-4572-491c-85e9-33ceed2cd753.png)

El tamaño de la memoria caché y la hora de expiración de las entradas de caché se establecen a través de claves del Registro. Para obtener información sobre cómo configurar estas claves del Registro, vea [Crear y configurar particiones COM+.](creating-and-configuring-com--partitions.md)

> [!Note]  
> Si un equipo servidor está desconectado de la red y la asignación de usuario a partición cambia mientras el servidor está desconectado, la caché de particiones podría contener una asignación de usuario a partición obsoleta. Esto podría producir un error de activación si la asignación de usuario a partición es el mecanismo utilizado para activar un componente.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Buscar un componente para la activación](locating-a-component-for-activation.md)
</dt> </dl>

 

