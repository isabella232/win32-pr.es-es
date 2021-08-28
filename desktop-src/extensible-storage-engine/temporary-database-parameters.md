---
description: 'Más información sobre: Parámetros temporales de base de datos'
title: Parámetros temporales de base de datos
TOCTitle: Temporary Database Parameters
ms:assetid: fa1cd867-6ce4-4de5-b31d-5b886f7c1e77
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294140(v=EXCHG.10)
ms:contentKeyID: 32765754
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
ms.openlocfilehash: 427ed51c2757075ccb28fd70e5554c49dc8db4e8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986828"
---
# <a name="temporary-database-parameters"></a>Parámetros temporales de base de datos


_**Se aplica a:** Windows | Windows Servidor_

## <a name="temporary-database-parameters"></a>Parámetros temporales de base de datos

Este tema contiene parámetros que se usan para la base de datos temporal.

*JET_paramEnableTempTableVersioning*  
46  

Este parámetro controla el uso de transacciones en tablas temporales. Cuando este parámetro es false, las tablas temporales serán más rápidas, pero no será posible revertir las actualizaciones realizadas en una transacción.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>True</p> | 
| <p>Escriba:</p> | <p>Boolean</p> | 
| <p>Intervalo válido:</p> | <p>False, True</p> | 
| <p>Ámbito:</p> | <p>Instancia</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>Sí</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>Sí</p> | 
| <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramPageTempDBMin*  
19  

Este parámetro controla el tamaño inicial de la base de datos temporal. El tamaño está en páginas de base de datos. Un tamaño de cero indica que se debe usar el tamaño predeterminado de una base de datos normal.

A menudo es conveniente que las aplicaciones pequeñas configuren la base de datos temporal para que sea lo más pequeña posible. Si se establece este parámetro en 14, se logrará la base de datos temporal más pequeña posible. Tenga en cuenta que también se puede eliminar completamente la base de datos temporal **estableciendo JET_paramMaxTemporaryTables** en cero.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>0</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p>0 – 2147483647</p> | 
| <p>Ámbito:</p> | <p>Instancia</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>Sí</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>Sí</p> | 
| <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramTempPath*  
1  

Este parámetro indica la ruta de acceso del sistema de archivos relativa o absoluta de la carpeta o archivo que contendrá la base de datos temporal para la instancia. Si la ruta de acceso es a una carpeta que contendrá la base de datos temporal, debe terminarse con un carácter de barra diagonal inversa. La base de datos temporal se usa para contener datos volátiles que se generan en el proceso de control de llamadas de información de API de ESE, creación de índices o almacenamiento del contenido de una tabla temporal.

**Nota**  Si se especifica una ruta de acceso relativa, será relativa al directorio de trabajo actual del proceso que hospeda la aplicación que usa el motor de base de datos.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>"tmp.edb"</p> | 
| <p>Escriba:</p> | <p>Ruta de acceso (cadena)</p> | 
| <p>Intervalo válido:</p> | <p>De 0 a 247 caracteres</p> | 
| <p>Ámbito:</p> | <p>Instancia</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>Sí</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>No</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>All</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[Archivos extensibles Storage engine](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
