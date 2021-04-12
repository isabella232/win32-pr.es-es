---
description: La clase FOURCCMap proporciona conversión entre subtipos de medios GUID y etiquetas de medios de 32 bits FOURCC de estilo antiguo.
ms.assetid: f77f1da9-34f6-44a0-9f1a-7db2e5a26268
title: Clase FOURCCMap
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
ms.openlocfilehash: fd30a0f04d98b4c6ba4b7716a1a72d527873dbff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152346"
---
# <a name="fourccmap-class"></a>Clase FOURCCMap

![jerarquía de clases fourccmap](images/fourcc01.png)

La clase **FOURCCMap** proporciona conversión entre subtipos de medios **GUID** y etiquetas de medios de 32 bits **FourCC** de estilo antiguo. En las API multimedia originales de Windows, los tipos de medios se etiquetaron con valores de 32 bits creados a partir de caracteres de 4 8 bits y se conocían como **FourCC** s. Los tipos de medios de DirectShow tienen **GUID** s para el subtipo, en parte porque son más fáciles de crear (la creación de un nuevo **FourCC** requiere su registro en Microsoft). Dado que los **FourCC** son únicos, se ha hecho una asignación uno a uno asignando un intervalo de 4 mil millones **GUID** que representan los **FourCC**. Este intervalo son todos los **GUID** del formulario:

`XXXXXXXX-0000-0010-8000-00AA00389B71`

Esta clase simplifica la conversión entre **GUID** s y **FourCC** s. Esto es solo por compatibilidad. Se recomienda que todos los subtipos de medios nuevos estén representados por **GUID** s creados por Guidgen.exe o una herramienta similar, y no por la asignación de **FourCC** s.

El objeto se deriva de un **GUID**, sin miembros de datos adicionales, y se puede convertir en un **GUID**. El objeto se puede pasar a **FourCC** en el momento de la construcción. El constructor predeterminado inicializará el **FourCC** en cero.

Los métodos [**GetFOURCC**](fourccmap-getfourcc.md) y [**SetFOURCC**](fourccmap-setfourcc.md) no comprueban que las partes fijas del **GUID** se correspondan con el intervalo de **FourCC** . Por lo tanto, si convierte un puntero en un **GUID** en un puntero a un **FourCC** y, a continuación, establece u obtiene el campo **FourCC** , también debe comprobar por separado que el **GUID** está dentro del intervalo de **FourCC** .

## <a name="member-functions"></a>Funciones de miembro



|                                          |                                                          |
|------------------------------------------|----------------------------------------------------------|
| [**FOURCCMap**](fourccmap-fourccmap.md) | Método de constructor.                                      |
| [**GetFOURCC**](fourccmap-getfourcc.md) | Recupera el **FourCC** de un objeto **FOURCCMap** .    |
| [**SetFOURCC**](fourccmap-setfourcc.md) | Establece la parte **FourCC** del objeto **FOURCCMap** . |



 

 

 



