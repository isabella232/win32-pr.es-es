---
description: Contiene información que se usa para crear un contexto de Tablet PC.
ms.assetid: 10466c23-f4cb-4205-886b-d85a2f530afe
title: Estructura de TABLET_CONTEXT_SETTINGS
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
ms.openlocfilehash: 9357281409ed4c48b4c6013a7a2be2997d58b094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003069"
---
# <a name="tablet_context_settings-structure"></a>Estructura de configuración de \_ contexto de Tablet \_

Contiene información que se usa para crear un contexto de Tablet PC.

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

El número de propiedades de un paquete.

</dd> <dt>

**pguidPktProps**
</dt> <dd>

Identificadores únicos para las propiedades de paquete.

</dd> <dt>

**cPktBtns**
</dt> <dd>

Número de botones.

</dd> <dt>

**pguidPktBtns**
</dt> <dd>

Identificadores únicos para los botones.

</dd> <dt>

**pdwBtnDnMask**
</dt> <dd>

La máscara del botón hacia abajo.

</dd> <dt>

**pdwBtnUpMask**
</dt> <dd>

La máscara del botón arriba.

</dd> <dt>

**lXMargin**
</dt> <dd>

Margen de la dirección X.

</dd> <dt>

**lYMargin**
</dt> <dd>

Margen de dirección Y.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Normalmente, una aplicación obtiene los valores predeterminados del [**método ITablet:: GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifica los valores para satisfacer sus necesidades y, a continuación, pasa la estructura de configuración modificada al [**método ITablet:: CreateContext**](itablet-createcontext.md).

Esta estructura determina qué eventos obtendrá una aplicación, cómo se procesarán y cómo se entregarán a la aplicación o a Windows.

Las máscaras de botón juntas determinan qué tipos de eventos se procesarán en el contexto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                     |



 

 




