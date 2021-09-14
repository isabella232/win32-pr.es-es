---
description: 'Más información sobre: JET_RSTINFO estructura'
title: JET_RSTINFO estructura
TOCTitle: JET_RSTINFO Structure
ms:assetid: 2f144d68-dcd9-4d0d-9d9e-a7d2a5c350fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269216(v=EXCHG.10)
ms:contentKeyID: 32765519
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
ms.openlocfilehash: 76da8fdc7ded6025e2497771622a8e34c3928967
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965596"
---
# <a name="jet_rstinfo-structure"></a>JET_RSTINFO estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_rstinfo-structure"></a>JET_RSTINFO estructura

La **estructura JET_RSTINFO** contiene información de control para el proceso de recuperación, como la información de reubicación de la base de datos y la capacidad de controlar la detención de la recuperación.

**Windows Vista:** La **JET_RSTINFO** estructura se introduce en Windows Vista.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_RSTMAP* rgrstmap;
      long crstmap;
      JET_LGPOS lgposStop;
      JET_LOGTIME logtimeStop;
      JET_PFNSTATUS pfnStatus;
    } JET_RSTINFO;
```

### <a name="members"></a>Members

**cbStruct**

Tamaño de la estructura.

**rgrstmap**

Estructura que describe la ruta de acceso antigua y nueva de una base de datos restaurada.

**crstmap**

Recuento de entradas de matriz en el gráfico rgrstmap.

**lgposStop**

Posición del registro en la que se detiene la recuperación. No se realizará ninguna deshacer.

**logtimeStop**

Reservado para uso futuro.

**pfnStatus**

Función de estado para notificar el estado de recuperación.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JET_RSTINFO_W</strong> (Unicode) <strong>y JET_RSTINFO_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte también

[JetInit3](./jetinit3-function.md)
