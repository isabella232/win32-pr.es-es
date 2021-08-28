---
description: 'Más información sobre: Enumeración StopServiceGrbit'
title: Enumeración StopServiceGrbit (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: StopServiceGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.stopservicegrbit(v=EXCHG.10)
ms:contentKeyID: 55104330
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6c8280bf4abfbc9eb5818d1aab460a17298db7b0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477461"
---
# <a name="stopservicegrbit-enumeration"></a>StopServiceGrbit (enumeración)

Opciones para [JetStopServiceInstance2(JET_INSTANCE, StopServiceGrbit).](./windows8api.jetstopserviceinstance2-method.md)

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration StopServiceGrbit
'Usage
Dim instance As StopServiceGrbit
```

``` csharp
[FlagsAttribute]
public enum StopServiceGrbit
```

## <a name="members"></a>Miembros


|  | Nombre del miembro | Descripción | 
|--|-------------|-------------|
|  | Todo | Detiene todos los servicios ese para la instancia especificada. | 
|  | BackgroundUserTasks | Detiene las tareas de mantenimiento en segundo plano específicas del cliente reiniciables (desfragmentación de árbol B+). | 
|  | QuiesceCaches | Se desasocian todas las cachés desasembladas en el disco. Asincrónica La anulación de la actividad se cancela si se llama al bit Reanudar posteriormente. | 
|  | Reanudar | Reanuda las operaciones StopService emitidas anteriormente, es decir, "reinicia el servicio". Se puede combinar con los bits grbits anteriores para reanudar servicios específicos o con 0x0 reanuda todos los servicios detenidos anteriores.<p>Advertencia: Este bit solo se puede usar para reanudar JET_bitStopServiceBackground y JET_bitStopServiceQuiesceCaches, si ha hecho una JET_bitStopServiceAll o JET_bitStopServiceAPI, se producirá un error al intentar usar JET_bitStopServiceResume.</p> | 



## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
