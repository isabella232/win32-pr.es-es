---
description: Contiene atributos de recurso compartido DDE mantenidos por el Administrador de bases de datos de recursos compartidos de NetDDE (DSDM).
ms.assetid: f4101553-06ef-4f83-87c7-5b6fdf0467e5
title: Estructura NDDESHAREINFO (Nddeapi.h)
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
ms.openlocfilehash: 84d29bcf5e1e4d086ca60da619edf26640c583f238d4fa956b3edd696eceee1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481715"
---
# <a name="nddeshareinfo-structure"></a>Estructura NDDESHAREINFO

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ NOT \_ IMPLEMENTED.\]

Contiene atributos de recurso compartido DDE mantenidos por el Administrador de bases de datos de recursos compartidos de NetDDE (DSDM). El descriptor de seguridad asociado a cada recurso compartido DDE no se pasa a través de esta estructura, pero se accede a través de funciones específicas. La API de DSDM de NetDDE acepta esta estructura para las funciones establecidas. Para las funciones get, DSDM devuelve la estructura empaquetada en el búfer proporcionado junto con los datos a los que hacen referencia los miembros **lpszShareName**, **lpszAppTopicList** y **lpszItemList**.

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

Nivel de revisión de la **estructura NDDESHAREINFO.** Actualmente, el nivel de revisión es 1.

</dd> <dt>

**lpszShareName**
</dt> <dd>

Nombre del recurso compartido. Esta cadena no debe tener más de MAX \_ NDDESHARENAME caracteres de longitud.

</dd> <dt>

**lShareType**
</dt> <dd>

Uno o varios tipos de recursos compartidos DDE. Este miembro puede ser una combinación de los siguientes tipos de recursos compartidos DDE admitidos.



| Tipo de recurso compartido                                                                                                                                                                                                                           | Significado                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SHARE_TYPE_NEW"></span><span id="share_type_new"></span><dl> <dt>**COMPARTIR \_ ESCRIBA \_ NEW**</dt> <dt>0x02</dt> </dl>          | El recurso compartido contiene un par de aplicación OLE/tema.<br/>   |
| <span id="SHARE_TYPE_OLD"></span><span id="share_type_old"></span><dl> <dt>**COMPARTIR \_ TYPE \_ OLD**</dt> <dt>0x01</dt> </dl>          | El recurso compartido contiene un par de aplicación/tema DDE.<br/>    |
| <span id="SHARE_TYPE_STATIC"></span><span id="share_type_static"></span><dl> <dt>**COMPARTIR \_ TYPE \_ STATIC**</dt> <dt>0x04</dt> </dl> | El recurso compartido contiene un par de aplicación/tema estático.<br/> |



 

</dd> <dt>

**lpszAppTopicList**
</dt> <dd>

Puntero a un búfer que contiene cadenas terminadas en NULL para los pares DDE, OLE y static application/topic. El búfer debe tener el formato siguiente:

``` syntax
<DDE application name>|<DDE topic name>\0
<OLE application name>|<OLE topic name>\0
<static application name>|<static topic name>\0\0
```

</dd> <dt>

**fSharedFlag**
</dt> <dd>

Si este miembro es **FALSE,** el recurso compartido DDE no permitirá que los usuarios remotos se comuniquen a través de él mediante DDE. Sin embargo, los usuarios locales todavía pueden comunicarse a través del recurso compartido de DDE. Los vínculos de cliente local siempre están implícitos si la DACL asociada concede acceso.

</dd> <dt>

**fService**
</dt> <dd>

Si se establece este miembro, el recurso compartido DDE no comprobará si el usuario actual lo ha establecido como de confianza antes de permitir la comunicación con DDE.

</dd> <dt>

**fStartAppFlag**
</dt> <dd>

Si se establece este miembro y el recurso compartido es de confianza para iniciar aplicaciones, NetDDE intentará iniciar la aplicación especificada por **lpszAppTopicList** si no puede iniciar inicialmente una conversación de DDE con la aplicación.

</dd> <dt>

**nCmdShow**
</dt> <dd>

Cuando NetDDE inicia una aplicación para iniciar una conversación de DDE, este valor se envía a la aplicación a través del parámetro *nCmdShow* de la [**función WinMain.**](/windows/win32/api/winbase/nf-winbase-winmain) Define el modo preferido en el que se mostrará la ventana de la aplicación. Este parámetro solo es significativo si **fStartAppFlag** está activo. El usuario que ha iniciado sesión en cuyo contexto se inicia la aplicación también puede invalidar esta opción al promover el recurso compartido al estado de confianza. El valor predeterminado de este miembro es SW \_ SHOWMAXIMIZED.

</dd> <dt>

**qModifyId**
</dt> <dd>

Número de serie de 8 bytes que indica el número de serie de modificación del recurso compartido DDE. Cada vez que una llamada [**NDdeShareSetInfo**](nddesharesetinfo.md) o [**NDdeSetShareSecurity**](nddesetsharesecurity.md) modifica el recurso compartido de DDE, estos valores se cambian.

</dd> <dt>

**cNumItems**
</dt> <dd>

Número de elementos enumerados en **lpszItemList.** Si **cNumItems** es cero, **lpszItemList** está vacío y la información del recurso compartido y el descriptor de seguridad asociado se aplican a todos los elementos a los que atiende la aplicación asociada.

</dd> <dt>

**lpszItemList**
</dt> <dd>

Puntero a un búfer que contiene cadenas terminadas en NULL que especifican los elementos en los que la aplicación cliente de una transacción DDE puede solicitar o iniciar bucles de aviso. Si no aparece ningún elemento, el recurso compartido DDE permite usar cualquier elemento. El número de elementos de la lista debe coincidir con **el recuento de cNumItems.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Información general datos dinámicos Exchange red](network-dynamic-data-exchange.md)
</dt> <dt>

[Estructuras DDE de red](network-dde-structures.md)
</dt> <dt>

[**NDdeSetShareSecurity**](nddesetsharesecurity.md)
</dt> <dt>

[**NDdeShareSetInfo**](nddesharesetinfo.md)
</dt> <dt>

[**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain)
</dt> </dl>

 

