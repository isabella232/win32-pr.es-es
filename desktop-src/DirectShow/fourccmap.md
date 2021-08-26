---
description: La clase FOURCCMap proporciona la conversión entre subtipos de medios GUID y etiquetas multimedia fourcc de 32 bits de estilo antiguo.
ms.assetid: f77f1da9-34f6-44a0-9f1a-7db2e5a26268
title: FOURCCMap (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap
api_type:
- COM
api_location: ''
ms.openlocfilehash: a0ba22ce288535a8d940a5f70275f0152ffa559090d820b77df06ed3d1a9178d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043275"
---
# <a name="fourccmap-class"></a>FOURCCMap (clase)

![jerarquía de clases fourccmap](images/fourcc01.png)

La **clase FOURCCMap proporciona** la conversión entre subtipos de medios **GUID** y etiquetas multimedia **fourcc** de 32 bits de estilo antiguo. En las API Windows multimedia originales, los tipos de medios se etiquetaban con valores de 32 bits creados a partir de cuatro caracteres de 8 bits y se conocían como **FOURCC.** DirectShow los tipos multimedia tienen **GUID** para el subtipo, en parte porque son más fáciles de crear (la creación de un **nuevo FOURCC** requiere su registro con Microsoft). Dado **que los FOURCC** son únicos, se ha hecho posible una asignación uno a uno mediante la asignación de un intervalo de 4000 millones **de GUID** que representan **FOURCC** s. Este intervalo tiene todos **los GUID** del formulario:

`XXXXXXXX-0000-0010-8000-00AA00389B71`

Esta clase simplifica la conversión entre **GUID** y **FOURCC.** Esto es solo por compatibilidad. Se recomienda que todos los nuevos subtipos de medios se represente mediante **GUID** creados por Guidgen.exe o una herramienta similar, y no mediante la asignación **de FOURCC** s.

El objeto se deriva de un **GUID**, sin miembros de datos adicionales, y se puede convertir a un **GUID**. Se puede pasar un **FOURCC al** objeto en tiempo de construcción. El constructor predeterminado inicializará **fourcc** en cero.

Los [**métodos GetFOURCC**](fourccmap-getfourcc.md) y [**SetFOURCC**](fourccmap-setfourcc.md) no comprueban que las partes fijas del **GUID** se correspondan con **el intervalo FOURCC.** Por lo tanto, si convierte un puntero a un **GUID** en un puntero a **un FOURCC** y, a continuación, establece u obtiene el **campo FOURCC,** también debe comprobar por separado que el **GUID** está dentro del **intervalo FOURCC.**

## <a name="member-functions"></a>Funciones de miembro



| Etiqueta | Value |
|------------------------------------------|----------------------------------------------------------|
| [**FOURCCMap**](fourccmap-fourccmap.md) | Método constructor.                                      |
| [**GetFOURCC**](fourccmap-getfourcc.md) | Recupera el **FOURCC** de un **objeto FOURCCMap.**    |
| [**SetFOURCC**](fourccmap-setfourcc.md) | Establece la **parte FOURCC** del **objeto FOURCCMap.** |



 

 

 



