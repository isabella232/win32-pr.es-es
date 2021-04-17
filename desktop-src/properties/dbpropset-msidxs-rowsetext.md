---
description: Extiende las propiedades definidas para las API del conjunto de filas.
ms.assetid: C1A2DF19-C68D-42CC-9CB2-190F22CB4158
title: DBPROPSET_MSIDXS_ROWSETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba37466c52f2fa9f83e3aa439ace03c1fba34f44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706885"
---
# <a name="dbpropset_msidxs_rowsetext"></a>DBPROPSET \_ MSIDXS \_ ROWSETEXT

Extiende las propiedades definidas para las API del conjunto de filas.

``` syntax
#define DBPROPSET_MSIDXS_ROWSETEXT \
    { 0xaa6ee6b0, 0xe828, 0x11d0, \
        { 0xb2, 0x3e, 0x00, 0xaa, 0x00, 0x47, 0xfc, 0x01 } }
```

El \_ conjunto de propiedades DBPROPSET MSIDXS \_ ROWSETEXT contiene las siguientes constantes de propiedad:

<dl> <dt>

<span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>MSIDXSPROP \_ ROWSETQUERYSTATUS
</dt> <dd>

IDENTIFICADOR de propiedad 2. Estado de la consulta para el conjunto de filas. Las constantes de STAT \_ \* indican la ejecución y el estado de confiabilidad.

</dd> <dt>

<span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>\_cadena de \_ configuración regional del comando MSIDXSPROP \_
</dt> <dd>

IDENTIFICADOR de propiedad 3. Cadena de configuración regional que representa la configuración regional y de idioma que se va a usar para este conjunto de filas.

</dd> <dt>

<span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>\_restricción de consulta MSIDXSPROP \_
</dt> <dd>

IDENTIFICADOR de propiedad 4. Cadena de consulta asociada a este conjunto de filas.

</dd> <dt>

<span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>\_árbol de análisis de MSIDXSPROP \_
</dt> <dd>

IDENTIFICADOR de propiedad 5.

</dd> <dt>

<span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>\_rango máximo de MSIDXSPROP \_ 
</dt> <dd>

IDENTIFICADOR de propiedad 6.

</dd> <dt>

<span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>resultados de MSIDXSPROP \_ \_ encontrados
</dt> <dd>

IDENTIFICADOR de propiedad 7.

</dd> <dt>

<span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>MSIDXSPROP \_ WHEREID
</dt> <dd>

IDENTIFICADOR de propiedad 8.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>\_versión del servidor de MSIDXSPROP \_ 
</dt> <dd>

Novedades de Windows 7. IDENTIFICADOR de propiedad 9. La versión del servidor.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>MSIDXSPROP \_ Server \_ winver \_ major
</dt> <dd>

IDENTIFICADOR de propiedad 10.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>MSIDXSPROP \_ Server \_ winver \_ Minor
</dt> <dd>

IDENTIFICADOR de propiedad 11.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>MSIDXSPROP \_ Server \_ NLSVERSION
</dt> <dd>

IDENTIFICADOR de propiedad 12.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>MSIDXSPROP \_ Server \_ NLSVER \_ DEFINED 
</dt> <dd>

IDENTIFICADOR de propiedad 13.

</dd> <dt>

<span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>MSIDXSPROP \_ mismo \_ orden \_ usado 
</dt> <dd>

IDENTIFICADOR de propiedad 14.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para consultar la \_ versión del servidor de MSIDXSPROP \_ , es necesario emitir la consulta ficticia en el servidor, como en el ejemplo siguiente.

`SELECT top 1 workid from servername.systemindex`

Una vez devuelto el conjunto de filas, llame a [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener las capacidades del conjunto de filas y, a continuación, llame a [IRowsetInfo:: GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) para la nueva propiedad (MSIDXSPROP \_ Server \_ version). La propiedad tiene un tipo de **VT \_ I4** y puede tener uno de los valores siguientes:

\#definir la \_ versión de CI \_ WDS30 0x102//258

\#definir la \_ versión de CI \_ WDS40 0x109//265

\#definir la \_ versión de CI \_ WIN70 0x700//1792

Una vez que se conoce el valor, el cliente puede crear una consulta que sea compatible con el servidor y emitir una consulta real.

DBPROPSET \_ MSIDXS \_ ROWSETEXT se declara en NTQuery. h.

 

 
