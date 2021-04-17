---
description: Aunque existen pocos límites técnicos para el tipo y el tamaño de los datos que una aplicación puede almacenar en el registro, existen ciertas directrices prácticas para fomentar la eficacia del sistema.
ms.assetid: fa85ff87-3d72-4f71-856a-f43df7d19aa8
title: Espacio de almacenamiento del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b776498528d6c7deaacd92f9e010758b5d57c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667588"
---
# <a name="registry-storage-space"></a>Espacio de almacenamiento del registro

Aunque existen pocos límites técnicos para el tipo y el tamaño de los datos que una aplicación puede almacenar en el registro, existen ciertas directrices prácticas para fomentar la eficacia del sistema. Una aplicación debe almacenar los datos de inicialización y configuración en el registro y almacenar otros tipos de datos en otra ubicación.

Por lo general, los datos que se componen de más de uno o dos kilobytes (K) deben almacenarse como un archivo y se hace referencia a ellos mediante una clave en el registro en lugar de almacenarse como un valor. En lugar de duplicar grandes fragmentos de datos en el registro, una aplicación debe guardar los datos como un archivo y hacer referencia al archivo. El código binario ejecutable nunca debe almacenarse en el registro.

Una entrada de valor utiliza mucho menos espacio de registro que una clave. Para ahorrar espacio, una aplicación debe agrupar datos similares como una estructura y almacenar la estructura como un valor en lugar de almacenar cada uno de los miembros de la estructura como una clave independiente. (Almacenar los datos en formato binario permite a una aplicación almacenar datos en un valor que, de otro modo, se compone de varios tipos incompatibles).

Las vistas de los archivos del registro se asignan en la memoria del grupo paginado.

**Windows server 2008 para 32 bits, Windows Vista con SP1 para 32 bits, Windows Vista, Windows Server 2003 y Windows XP:** Las vistas de los archivos de registro se asignan en el espacio de direcciones de caché del equipo. Por lo tanto, independientemente del tamaño de los datos del registro, no se le cobrarán más de 4 megabytes (MB).

El tamaño máximo de un subárbol del registro es 2 GB, excepto el subárbol del sistema.

**Windows server 2003 con SP1, Windows server 2003 y Windows XP:** No hay ningún límite explícito en la cantidad total de espacio que pueden consumir los subárboles en la memoria del grupo paginado y en el espacio en disco, aunque las cuotas del sistema pueden afectar al tamaño máximo real. El tamaño máximo de un subárbol del registro estaba limitado a 2 GB a partir de Windows Server 2003 con Service Pack 2 (SP2).

El tamaño máximo del subárbol del sistema está limitado por la memoria física, tal como se muestra en la tabla siguiente. 

| System                      | Tamaño máximo del subárbol del sistema                                                                                                                                                                                                            |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sistemas basados en x86           | 50 por ciento de la memoria física, hasta 400 MB. **Windows server 2003 con SP2, Windows server 2003 con SP1, Windows server 2003 y Windows XP:** 25 por ciento de memoria física, hasta 200 MB.<br/>                                    |
| sistemas basados en x64           | 50 por ciento de la memoria física, hasta 1,5 GB. **Windows Server 2003 con SP2:** 25 por ciento de la memoria del sistema, hasta 200 MB.<br/> **Windows server 2003 con SP1, Windows server 2003 y Windows XP 64-bit Edition:** 32 MB.<br/> |
| Sistemas basados en Itanium de Intel | 50 por ciento de la memoria física, hasta 1 GB. **Windows server 2008, Windows Vista, Windows server 2003 con SP2, Windows server 2003 con SP1, Windows server 2003 y Windows XP 64-bit Edition:** 32 MB.<br/>                         |



 

## <a name="windows-2000"></a>Windows 2000

Los datos del registro se almacenan en el grupo paginado, un área de memoria física que se usa para los datos del sistema que se pueden escribir en el disco cuando no están en uso. El valor **RegistrySizeLimit** establece la cantidad máxima de bloque paginado que pueden consumir los datos del registro de todas las aplicaciones. Este valor se encuentra en la siguiente clave del registro:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
```

De forma predeterminada, el límite de tamaño del registro es el 25 por ciento del grupo paginado. (El tamaño predeterminado del grupo paginado es 32 MB, por lo que es de 8 MB). El sistema garantiza que el valor mínimo de **RegistrySizeLimit** es 4 MB y el máximo es aproximadamente el 80 por ciento del valor de **PagedPoolSize** . Si el valor de esta entrada es superior al 80 por ciento del tamaño del grupo paginado, el sistema establece el tamaño máximo del registro en el 80 por ciento del tamaño del grupo paginado. Esto impide que el registro consuma el espacio necesario para los procesos. Tenga en cuenta que el establecimiento de este valor no asigna espacio en el grupo paginado, ni garantiza que el espacio estará disponible si es necesario.

El tamaño del grupo paginado viene determinado por el valor de **PagedPoolSize** en la siguiente clave del registro:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            SessionManager
               MemoryManagement
```

Para obtener un ejemplo de cómo determinar los tamaños actuales y máximos del registro, vea [determinar el tamaño del registro](determining-the-registry-size.md).

El grupo paginado máximo es de aproximadamente 300.470 MB, por lo que el límite de tamaño del registro es de 240-376 MB. Sin embargo, si se usa el modificador/3GB, el tamaño máximo del grupo paginado es 192 MB, por lo que el registro puede tener un máximo de 153,6 MB.

 

 




