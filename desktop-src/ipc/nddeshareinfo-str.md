---
description: Contiene atributos de recursos compartidos DDE mantenidos por el administrador de bases de datos de recursos compartidos (DSDM)
ms.assetid: f4101553-06ef-4f83-87c7-5b6fdf0467e5
title: Estructura NDDESHAREINFO (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDDESHAREINFO
api_type:
- HeaderDef
api_location:
- Nddeapi.h
ms.openlocfilehash: 975382272a4e2c7cc56b0ddf593905b4d745a48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707017"
---
# <a name="nddeshareinfo-structure"></a>Estructura NDDESHAREINFO

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

Contiene atributos de recursos compartidos DDE mantenidos por el administrador de bases de datos de recursos compartidos (DSDM) El descriptor de seguridad asociado a cada recurso compartido DDE no se pasa a través de esta estructura, pero se obtiene acceso a ella a través de funciones específicas. La API del DSDM de NetDDE acepta esta estructura para las funciones set. en el caso de las funciones Get, el DSDM devuelve la estructura empaquetada en el búfer suministrado junto con los datos a los que hacen referencia los miembros **lpszShareName**, **lpszAppTopicList** y **lpszItemList**.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _NDDESHAREINFO {
  LONG   lRevision;
  LPTSTR lpszShareName;
  LONG   lShareType;
  LPTSTR lpszAppTopicList;
  LONG   fSharedFlag;
  LONG   fService;
  LONG   fStartAppFlag;
  LONG   nCmdShow;
  LONG   qModifyId[2];
  LONG   cNumItems;
  LPTSTR lpszItemList;
} NDDESHAREINFO, *PNDDESHAREINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**lRevision**
</dt> <dd>

El nivel de revisión de la estructura **NDDESHAREINFO** . Actualmente, el nivel de revisión es 1.

</dd> <dt>

**lpszShareName**
</dt> <dd>

Nombre del recurso compartido. Esta cadena no debe tener más de \_ NDDESHARENAME caracteres como máximo.

</dd> <dt>

**lShareType**
</dt> <dd>

Uno o más tipos de recursos compartidos DDE. Este miembro puede ser una combinación de los siguientes tipos de recursos compartidos DDE admitidos.



| Tipo de recurso compartido                                                                                                                                                                                                                           | Significado                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SHARE_TYPE_NEW"></span><span id="share_type_new"></span><dl> <dt>**Recurso compartido \_ Escriba \_ nuevo**</dt> <dt>0x02</dt> </dl>          | El recurso compartido contiene un par aplicación/tema de OLE.<br/>   |
| <span id="SHARE_TYPE_OLD"></span><span id="share_type_old"></span><dl> <dt>**Recurso compartido \_ Escriba \_ Old**</dt> <dt>0x01</dt> </dl>          | El recurso compartido contiene un par aplicación/tema de DDE.<br/>    |
| <span id="SHARE_TYPE_STATIC"></span><span id="share_type_static"></span><dl> <dt>**Recurso compartido \_ Escriba \_ static**</dt> <dt>0x04</dt> </dl> | El recurso compartido contiene un par aplicación/tema estático.<br/> |



 

</dd> <dt>

**lpszAppTopicList**
</dt> <dd>

Un puntero a un búfer que contiene cadenas terminadas en null para los pares de aplicación/tema estáticos y de DDE. El búfer debe tener el formato siguiente:

``` syntax
<DDE application name>|<DDE topic name>\0
<OLE application name>|<OLE topic name>\0
<static application name>|<static topic name>\0\0
```

</dd> <dt>

**fSharedFlag**
</dt> <dd>

Si este miembro es **false**, el recurso compartido DDE no permitirá que los usuarios remotos se comuniquen mediante el uso de DDE. Sin embargo, los usuarios locales pueden seguir comunicándose a través del recurso compartido DDE. Los vínculos de cliente local siempre están implícitos si la DACL asociada concede acceso.

</dd> <dt>

**fService**
</dt> <dd>

Si se establece este miembro, el recurso compartido DDE no comprobará si el usuario actual lo ha establecido como de confianza antes de permitir la comunicación DDE.

</dd> <dt>

**fStartAppFlag**
</dt> <dd>

Si este miembro está establecido y el recurso compartido es de confianza para iniciar aplicaciones, NetDDE intentará iniciar la aplicación especificada por **lpszAppTopicList** si no puede iniciar inicialmente una conversación DDE con la aplicación.

</dd> <dt>

**nCmdShow**
</dt> <dd>

Cuando NetDDE inicia una aplicación para iniciar una conversación DDE, este valor se envía a la aplicación a través del parámetro *nCmdShow* de la función [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) . Define el modo preferido de la ventana de la aplicación que se va a mostrar en. Este parámetro solo es significativo si **fStartAppFlag** está activo. El usuario que ha iniciado sesión en cuyo contexto se inicia la aplicación también puede invalidar esta opción al promover el recurso compartido a estado de confianza. El valor predeterminado para este miembro es SW \_ SHOWMAXIMIZED.

</dd> <dt>

**qModifyId**
</dt> <dd>

Número de serie de 8 bytes que indica el número de serie de modificación del recurso compartido DDE. Cada vez que el recurso compartido DDE se modifica mediante una llamada a [**NDdeShareSetInfo**](nddesharesetinfo.md) o [**NDdeSetShareSecurity**](nddesetsharesecurity.md) , se cambian estos valores.

</dd> <dt>

**cNumItems**
</dt> <dd>

El número de elementos enumerados en **lpszItemList**. Si **cNumItems** es cero, **lpszItemList** está vacío y la información del recurso compartido y el descriptor de seguridad asociado se aplican a todos los elementos a los que presta servicio la aplicación asociada.

</dd> <dt>

**lpszItemList**
</dt> <dd>

Un puntero a un búfer que contiene cadenas terminadas en null que especifican los elementos en los que la aplicación cliente de una transacción DDE puede solicitar o iniciar bucles de notificaciones. Si no hay ningún elemento en la lista, el recurso compartido DDE permite el uso de cualquier elemento. El número de elementos de la lista debe coincidir con el recuento de **cNumItems** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general de Intercambio dinámico de datos de red](network-dynamic-data-exchange.md)
</dt> <dt>

[Estructuras DDE de red](network-dde-structures.md)
</dt> <dt>

[**NDdeSetShareSecurity**](nddesetsharesecurity.md)
</dt> <dt>

[**NDdeShareSetInfo**](nddesharesetinfo.md)
</dt> <dt>

[**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain)
</dt> </dl>

 

