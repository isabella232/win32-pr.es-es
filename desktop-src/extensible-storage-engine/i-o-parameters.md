---
description: 'Más información sobre: Parámetros de E/S'
title: Parámetros de E/S
TOCTitle: I/O Parameters
ms:assetid: 5df3c106-52ac-4ca0-9a6a-d5d62576bb23
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269260(v=EXCHG.10)
ms:contentKeyID: 32765562
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
ms.openlocfilehash: 62cc1183f14e3de113ff5f34eaf6367bc2ff0f9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568296"
---
# <a name="io-parameters"></a>Parámetros de E/S


_**Se aplica a:** Windows | Windows Servidor_

## <a name="io-parameters"></a>Parámetros de E/S

Este tema contiene parámetros que se usan para la entrada y salida (E/S).

*JET_paramAccessDeniedRetryPeriod*  
53  

**Windows XP y versiones posteriores:**  Este parámetro configura la duración del tiempo (en milisegundos) que usará el motor de base de datos para acceder a un archivo que está bloqueado antes de que se JET_errFileAccessDenied. Este retraso de tiempo está diseñado para evitar el software antivirus que puede contener algunos de los archivos del motor de base de datos abiertos brevemente después de cerrarse.

**Nota**  Como resultado de la lógica de reintento anterior, cualquier intento de adjuntar a una base de datos o usar un archivo de registro que ya está en uso por el motor de base de datos provocará un retraso de este tamaño antes de que la llamada API devuelva un error (legítimo). Este parámetro se puede usar para desactivar ese retraso en caso de que se trata de un escenario común.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>10000</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p>0 – 4294967295</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>Sí</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>Sí</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>Windows XP y versiones posteriores</p> | 



*JET_paramCreatePathIfNotExist*  
100  

Cuando este parámetro se establece en true, cualquier carpeta que falte en una ruta de acceso del sistema de archivos en uso por el motor de base de datos se creará en modo silencioso. De lo contrario, se producirá un error en la operación que usa la ruta de acceso del sistema de archivos que falta JET_errInvalidPath.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>False</p> | 
| <p>Escriba:</p> | <p>Boolean</p> | 
| <p>Intervalo válido:</p> | <p>False, True</p> | 
| <p>Ámbito:</p> | <p>Instancia</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>Sí</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>No</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramEnableFileCache*  
126  

Cuando este parámetro es **True,** el motor de base de datos usará la caché de archivos Windows como caché de lectura para todos sus distintos archivos. También la usará como caché de escritura para la base de datos temporal o para las bases de datos que se abren con la recuperación deshabilitada. El motor de base de datos debe deshabilitar el almacenamiento en caché de escritura para bases de datos normales, archivos de registro de transacciones y archivos de punto de comprobación para proteger la integridad transaccional de las bases de datos.

Es importante tener en cuenta que el uso de la caché de archivos Windows agregará una segunda capa de almacenamiento en caché para los archivos de base de datos. La caché de base de datos seguirá utilizando su propia memoria para almacenar en caché los archivos de base de datos. La intención de este modo es permitir que la aplicación configure el motor de base de datos con una pequeña caché dedicada y permitir que Windows resalte la memoria de reserva para mejorar aún más el almacenamiento en caché de los datos de la base de datos.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>False</p> | 
| <p>Escriba:</p> | <p>Boolean</p> | 
| <p>Intervalo válido:</p> | <p>False, True</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>Sí</p> | 
| <p>Disponibilidad:</p> | <p>Windows Vista y versiones posteriores</p> | 



*JET_paramIOPriority*  
152  

Este parámetro controla cómo ese controla las operaciones de E/S. Los valores se pueden establecer en 0 (JET_IOPriorityNormal) para el funcionamiento normal o 1 (JET_IOPriorityLow) para la operación de prioridad baja. Cuando la prioridad se establece en JET_IOPriorityLow, ESE usa la nueva funcionalidad de prioridad de E/S de subproceso disponible en Windows Vista para reducir la prioridad de E/S en el subproceso para que las operaciones de E/S posteriores se emita con la nueva prioridad baja.

**Windows Vista:**  JET_paramIOPriority se introdujo en Windows Vista.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>0</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p>0 - 1</p> | 
| <p>Ámbito:</p> | <p>Instancia</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>Sí</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>Windows Vista</p> | 



*JET_paramOutstandingIOMax*  
30 

Este parámetro controla cuántas E/S de archivo de base de datos se pueden poner en cola en el sistema operativo host a la vez.

Un valor mayor para este parámetro puede ayudar significativamente al rendimiento de una aplicación de base de datos grande.

**Windows XP y Windows Server 2003:**  Este parámetro se omite en Windows XP y Windows Server 2003 y no afecta al funcionamiento del motor de base de datos.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p><strong>Windows 2000:</strong> 64</p><p><strong>Windows Vista:</strong> 1024</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 8 – 2147483647</p><p><strong>Windows Vista:</strong> 0 – 65536</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>Sí</p> | 
| <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramMaxCoalesceReadSize*  
164  

Número máximo de bytes que se pueden agrupar para una operación de lectura coalesced.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>262 144</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p>0-1073741824</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceWriteSize*  
165  

Número máximo de bytes que se pueden agrupar para una operación de escritura agrupada.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>393216</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p>0-1073741824</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceReadGapSize*  
166  

Número máximo de bytes que se pueden acodar para una operación de E/S de escritura coalesced.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>262 144</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p>0-1073741824</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceWriteGapSize*  
167  

Número máximo de bytes que se pueden acodir para una operación de E/S de lectura desenlazado.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>393216</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p>0-1073741824</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>Windows 7</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
