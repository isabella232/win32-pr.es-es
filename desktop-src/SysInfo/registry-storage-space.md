---
description: Aunque hay pocos límites técnicos en el tipo y el tamaño de los datos que una aplicación puede almacenar en el registro, existen ciertas directrices prácticas para promover la eficacia del sistema.
ms.assetid: fa85ff87-3d72-4f71-856a-f43df7d19aa8
title: Espacio de Storage registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00414edbd34452fd6943a4d73a2ebe85af5d38884ddd0ca77f1d8fb41ae6e0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885083"
---
# <a name="registry-storage-space"></a>Espacio de Storage registro

Aunque hay pocos límites técnicos en el tipo y el tamaño de los datos que una aplicación puede almacenar en el registro, existen ciertas directrices prácticas para promover la eficacia del sistema. Una aplicación debe almacenar datos de configuración e inicialización en el Registro y almacenar otros tipos de datos en otro lugar.

Por lo general, los datos que constan de más de uno o dos kilobytes (K) se deben almacenar como un archivo y se debe hacer referencia a ellos mediante una clave en el registro en lugar de almacenarse como un valor. En lugar de duplicar grandes fragmentos de datos en el Registro, una aplicación debe guardar los datos como un archivo y hacer referencia al archivo. El código binario ejecutable nunca debe almacenarse en el Registro.

Una entrada de valor usa mucho menos espacio del Registro que una clave. Para ahorrar espacio, una aplicación debe agrupar datos similares como una estructura y almacenar la estructura como un valor en lugar de almacenar cada uno de los miembros de la estructura como una clave independiente. (Almacenar los datos en formato binario permite que una aplicación almacene datos en un valor que, de lo contrario, se conste de varios tipos incompatibles).

Las vistas de los archivos del Registro se asignan en la memoria del grupo paginado.

**Windows Server 2008 para 32 bits, Windows Vista con SP1 para 32 bits, Windows Vista, Windows Server 2003, Windows XP:** Las vistas de los archivos del Registro se asignan en el espacio de direcciones de caché del equipo. Por lo tanto, independientemente del tamaño de los datos del Registro, no se cobran más de 4 megabytes (MB).

El tamaño máximo de un subárbol del Registro es de 2 GB, excepto el subárbol del sistema.

**Windows Server 2003 con SP1, Windows Server 2003 y Windows XP:** No hay límites explícitos en la cantidad total de espacio que pueden consumir los subárboles en la memoria del grupo paginado y en el espacio en disco, aunque las cuotas del sistema pueden afectar al tamaño máximo real. El tamaño máximo de un subárbol del Registro estaba limitado a 2 GB a partir de Windows Server 2003 con Service Pack 2 (SP2).

El tamaño máximo del subárbol del sistema está limitado por la memoria física, como se muestra en la tabla siguiente. 

| Sistema                      | Tamaño máximo del subárbol del sistema                                                                                                                                                                                                            |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sistemas basados en x86           | 50 por ciento de memoria física, hasta 400 MB. **Windows Server 2003 con SP2, Windows Server 2003 con SP1, Windows Server 2003 y Windows XP:** 25 por ciento de memoria física, hasta 200 MB.<br/>                                    |
| Sistemas basados en x64           | 50 por ciento de memoria física, hasta 1,5 GB. **Windows Server 2003 con SP2:** 25 por ciento de memoria del sistema, hasta 200 MB.<br/> **Windows Server 2003 con SP1, Windows Server 2003 y Windows XP de 64** bits Edition: 32 MB.<br/> |
| Sistemas basados en Intel Itanium | 50 por ciento de memoria física, hasta 1 GB. **Windows Server 2008, Windows Vista, Windows Server 2003 con SP2, Windows Server 2003 con SP1, Windows Server 2003 y Windows XP edición de 64 bits:** 32 MB.<br/>                         |



 

## <a name="windows-2000"></a>Windows 2000

Los datos del Registro se almacenan en el grupo paginado, un área de memoria física que se usa para los datos del sistema que se pueden escribir en el disco cuando no se usan. El **valor RegistrySizeLimit** establece la cantidad máxima de grupo paginado que pueden consumir los datos del Registro de todas las aplicaciones. Este valor se encuentra en la siguiente clave del Registro:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
```

De forma predeterminada, el límite de tamaño del Registro es del 25 por ciento del grupo paginado. (El tamaño predeterminado del grupo paginado es de 32 MB, por lo que es 8 MB). El sistema garantiza que el valor mínimo de **RegistrySizeLimit** sea 4 MB y que el máximo sea aproximadamente el 80 % del **valor PagedPoolSize.** Si el valor de esta entrada es mayor que el 80 por ciento del tamaño del grupo paginado, el sistema establece el tamaño máximo del registro en el 80 por ciento del tamaño del grupo paginado. Esto evita que el registro consuma el espacio necesario para los procesos. Tenga en cuenta que al establecer este valor no se asigna espacio en el grupo paginado ni se garantiza que el espacio estará disponible si es necesario.

El tamaño del grupo paginado viene determinado por el **valor PagedPoolSize** de la siguiente clave del Registro:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            SessionManager
               MemoryManagement
```

Para obtener un ejemplo de cómo determinar los tamaños actual y máximo del registro, vea [Determinar el tamaño del Registro](determining-the-registry-size.md).

El grupo paginado máximo es de aproximadamente 300 470 MB, por lo que el límite de tamaño del registro es de 240 a 376 MB. Sin embargo, si se usa el modificador /3GB, el tamaño máximo del grupo paginado es de 192 MB, por lo que el registro puede ser un máximo de 153,6 MB.

 

 




