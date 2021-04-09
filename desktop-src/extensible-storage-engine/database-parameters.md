---
description: 'Más información acerca de: parámetros de base de datos'
title: Parámetros de base de datos
TOCTitle: Database Parameters
ms:assetid: 8fb68748-8718-4393-9fd6-0d9adaa34844
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269337(v=EXCHG.10)
ms:contentKeyID: 32765626
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8849096412fa77db107e3e866a20662bb2634665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155045"
---
# <a name="database-parameters"></a>Parámetros de base de datos


_**Se aplica a:** Windows | Windows Server_

## <a name="database-parameters"></a>Parámetros de base de datos

Este tema contiene los parámetros que se usan para la base de datos.

*JET_paramCheckFormatWhenOpenFail*  
44  

Si se establece este parámetro, [JetInit](./jetinit-function.md) devolverá un error especial cuando se abra una base de datos o un registro de transacciones de una versión anterior del motor de base de datos. Estos errores son:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Error</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errDatabase200Format</p></td>
<td><p>Los archivos de base de datos o de registro de transacciones se crearon con el motor de base de datos en Windows NT 3,51.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabase400Format</p></td>
<td><p>Los archivos de base de datos o de registro de transacciones se crearon con el motor de base de datos en una versión de prueba anterior a Windows NT Server 4,0.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase500Format</p></td>
<td><p>Los archivos de base de datos o de registro de transacciones se crearon con el motor de base de datos en Windows NT Server 4,0.</p></td>
</tr>
</tbody>
</table>


**Windows Vista:**  En Windows Vista y versiones posteriores, este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>True</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramDatabasePageSize*  
64  

Este parámetro configura el tamaño de página para la base de datos. El tamaño de página es la unidad más pequeña de asignación de espacio posible para un archivo de base de datos. El tamaño de página de la base de datos también es muy importante, ya que establece el límite superior del tamaño de un registro individual en la base de datos.

**Nota:** En este momento, solo se admite un tamaño de página de base de datos por proceso. Esto significa que, si se encuentra en un único proceso que contiene diferentes aplicaciones que usan el motor de base de datos, todos deben aceptar un tamaño de página de base de datos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>4096</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>2048, 4096, 8192</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramDbExtensionSize*  
18  

Este parámetro controla la cantidad de espacio que se agrega a un archivo de base de datos cada vez que necesita crecer para alojar más datos. El tamaño está en páginas de base de datos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>256</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>1 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p>
<p><strong>Windows Vista:</strong>  En Windows Vista y versiones posteriores: sí</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableIndexChecking*  
45  

Cuando este parámetro es true, todas las bases de datos se comprueban en el momento de la [JetAttachDatabase](./jetattachdatabase-function.md) para los índices de las columnas de clave Unicode compiladas con una versión anterior de la biblioteca NLS en el sistema operativo. Esto debe hacerse porque el motor de base de datos conserva las claves de ordenación generadas por [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) y el valor de estas claves de ordenación cambia de Release a Release.

Si se detecta que un índice principal está en este estado, [JetAttachDatabase](./jetattachdatabase-function.md) siempre producirá un error con JET_errPrimaryIndexCorrupted.

Si se detecta que algún índice secundario está en este estado, hay dos resultados posibles. Si JET_bitDbDeleteCorruptIndexes se pasó a [JetAttachDatabase](./jetattachdatabase-function.md) , estos índices se eliminarán y JET_wrnCorruptIndexDeleted se devolverán desde [JetAttachDatabase](./jetattachdatabase-function.md). Estos índices deberán volver a crearse en la aplicación. Si JET_bitDbDeleteCorruptIndexes no se pasó a [JetAttachDatabase](./jetattachdatabase-function.md) , se producirá un error en la llamada con JET_errSecondaryIndexCorrupted.

**Nota:** Se recomienda encarecidamente que la aplicación establezca este parámetro en true.

**Nota:** Se recomienda encarecidamente que las aplicaciones eviten el uso de columnas de clave Unicode en sus índices de clave principal (clúster).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p>
<p><strong>Windows Vista:</strong>  En Windows Vista y versiones posteriores: instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableIndexCleanup*  
54  

Cuando este parámetro se establece en true, el motor de base de datos puede limpiar automáticamente los índices de las columnas de clave Unicode en el tiempo de [JetInit](./jetinit-function.md) , según sea necesario, para evitar cambios en el formato de la base de datos causados por cambios en la biblioteca NLS de Windows. Estos cambios se realizan habitualmente en la biblioteca NLS para agregar compatibilidad con nuevos idiomas, agregar caracteres que faltan a un idioma, agregar un orden de intercalación a un idioma o corregir errores en el orden de intercalación de un idioma. Estos cambios afectan a los criterios de ordenación generados por [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) que el motor de base de datos conserva como componentes de las claves de índice.

Es importante saber que es posible que los cambios en el índice sean tan grandes que no sea posible realizar una limpieza incremental. En este caso, el índice se administrará como se indica en **JET_paramEnableIndexChecking**.

**Nota:** Se recomienda encarecidamente que la aplicación establezca este parámetro y **JET_paramEnableIndexChecking** en **true** .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>True</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p>
<p><strong>Windows Vista:</strong>  En Windows Vista y versiones posteriores: sí</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>Windows Server 2003 y versiones posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramOneDatabasePerSession*  
102  

Cuando este parámetro es true, solo se permite abrir una base de datos mediante [JetOpenDatabase](./jetopendatabase-function.md) por una sesión determinada al mismo tiempo. La base de datos temporal se excluye de esta restricción.

**Windows XP y Windows Server 2003:**  Este parámetro solo se escribe en Windows XP y Windows Server 2003.

**Windows Vista:**  Este parámetro se comporta normalmente a partir de Windows Vista.

**Nota:**  Este parámetro es de solo escritura.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p>
<p><strong>Windows Vista:</strong>  En Windows Vista y versiones posteriores: sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>Windows XP y versiones posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableOnlineDefrag*  
35  

Este parámetro controla el comportamiento de la desfragmentación con conexión cuando se inicia mediante [JetDefragment](./jetdefragment-function.md). Consulte [JetDefragment](./jetdefragment-function.md) para obtener más información.

Windows 2000: en Windows 2000, este parámetro era un valor booleano simple que canalizaría la desfragmentación en línea cuando lo inició [JetDefragment](./jetdefragment-function.md). Cuando se establece en **true**, la desfragmentación con conexión se realizará en los registros de cada tabla de la base de datos.

**Windows XP:**  En Windows XP y versiones posteriores, este parámetro se puede establecer en una o varias de las opciones siguientes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Opción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_OnlineDefragDisable</p></td>
<td><p>No lleve a cabo la desfragmentación en línea. Es el binario equivalente a la configuración de Windows 2000 de false para este parámetro.</p></td>
</tr>
<tr class="even">
<td><p>JET_OnlineDefragAllOBSOLETE</p></td>
<td><p>Realice una desfragmentación en línea completa. Es el binario equivalente a la configuración de Windows 2000 de true para este parámetro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_OnlineDefragDatabases</p></td>
<td><p>Realice una desfragmentación en línea de los registros de cada tabla en la base de datos.</p></td>
</tr>
<tr class="even">
<td><p>JET_OnlineDefragSpaceTrees</p></td>
<td><p>Realice una desfragmentación en línea de los árboles de espacio de cada tabla en la base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_OnlineDefragStreamingFiles</p></td>
<td><p>Este parámetro se usa para admitir la infraestructura de Microsoft Exchange y no está diseñado para usarse en la aplicación.</p></td>
</tr>
<tr class="even">
<td><p>JET_OnlineDefragAll</p></td>
<td><p>Realice una desfragmentación en línea completa. Este es el equivalente conceptual del valor de Windows 2000 de true para este parámetro.</p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p><strong>Windows 2000:</strong>  Reales</p>
<p><strong>Windows XP: para Windows XP y versiones posteriores:</strong> JET_OnlineDefragAll</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p><strong>Windows 2000:</strong>  Booleano</p>
<p><strong>Windows XP y versiones posteriores:</strong>  JET_GRBIT (entero)</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows 2000:</strong>  False, true</p>
<p><strong>Windows XP y versiones posteriores:</strong>  0: JET_OnlineDefragAll</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramPageFragment*  
20  

Este parámetro es el umbral que usa el motor de base de datos para controlar la fragmentación del espacio libre. El tamaño está en páginas de base de datos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>8</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>de 0 a 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramRecordUpgradeDirtyLevel*  
78

Este parámetro controla el modo en que el administrador de caché de páginas de base de datos escribirá una página de base de datos que se haya sometido a una conversión de formato en contexto. Estas conversiones de formato se producen sobre la marcha a medida que las páginas se cargan desde una base de datos que se creó con el motor de base de datos de Windows 2000, pero que usa Windows XP o una versión posterior del motor de base de datos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0-3</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>Windows XP y versiones posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramWaypointLatency*  
153  

La latencia (en registros) detrás del registro de propinas más alto para aplazar los vaciados de las páginas de la base de datos. La habilitación de esta latencia puede permitir la recuperación de bases de datos en caso de una pérdida catastrófica del archivo de registro más reciente. Vea JET_bitReplayIgnoreLostLogs.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0-1023</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramDefragmentSequentialBTrees*  
160  

Active o desactive la desfragmentación de árbol B secuencial automática.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0-1</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*  
161  

Determina la frecuencia con la que se comprueba la densidad del árbol B.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>10</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0: entero máximo</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramIOThrottlingTimeQuanta*  
162  

Tiempo máximo, en milisegundos, que el mecanismo de limitación de e/s permite que una tarea se ejecute para que se considere "completada".

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>125</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0-10000</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetInit](./jetinit-function.md)
