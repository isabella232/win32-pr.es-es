---
description: Contiene información utilizada para crear un contexto de tableta.
ms.assetid: 10466c23-f4cb-4205-886b-d85a2f530afe
title: TABLET_CONTEXT_SETTINGS estructura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_CONTEXT_SETTINGS
api_type:
- NA
api_location: ''
ms.openlocfilehash: 75634cd635773ff0b009860256b1147c31ee43dde200586e12713a707aa999b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119335085"
---
# <a name="tablet_context_settings-structure"></a>Estructura TABLET \_ CONTEXT \_ SETTINGS

Contiene información utilizada para crear un contexto de tableta.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _TABLET_CONTEXT_SETTINGS {
  ULONG cPktProps;
  GUID  *pguidPktProps;
  ULONG cPktBtns;
  GUID  *pguidPktBtns;
  DWORD *pdwBtnDnMask;
  DWORD *pdwBtnUpMask;
  LONG  lXMargin;
  LONG  lYMargin;
} TABLET_CONTEXT_SETTINGS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cPktProps**
</dt> <dd>

Número de propiedades de un paquete.

</dd> <dt>

**pguidPktProps**
</dt> <dd>

Identificadores únicos para las propiedades del paquete.

</dd> <dt>

**cPktBtns**
</dt> <dd>

Número de botones.

</dd> <dt>

**pguidPktBtns**
</dt> <dd>

Identificadores únicos de los botones.

</dd> <dt>

**pdwBtnDnMask**
</dt> <dd>

Máscara de botón hacia abajo.

</dd> <dt>

**pdwBtnUpMask**
</dt> <dd>

Máscara de botón hacia arriba.

</dd> <dt>

**lXMargin**
</dt> <dd>

Margen de dirección X.

</dd> <dt>

**lYMargin**
</dt> <dd>

Margen de dirección Y.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Normalmente, una aplicación obtiene los valores predeterminados del método [**ITablet::GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifica los valores para satisfacer sus necesidades y, a continuación, pasa la estructura de configuración modificada al método [**ITablet::CreateContext**](itablet-createcontext.md).

Esta estructura determina qué eventos recibirá una aplicación, cómo se procesarán y cómo se entregarán a la aplicación o a Windows sí misma.

Las máscaras de botón juntos determinan qué tipos de eventos procesará el contexto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                     |



 

 




