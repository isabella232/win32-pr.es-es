---
description: Extiende las propiedades definidas para las API de conjunto de filas.
ms.assetid: C1A2DF19-C68D-42CC-9CB2-190F22CB4158
title: DBPROPSET_MSIDXS_ROWSETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8c647d4b1ecbf9e5cc88ccae4af649c27093472456377e478ff80f7a76f3a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776415"
---
# <a name="dbpropset_msidxs_rowsetext"></a>DBPROPSET \_ MSIDXS \_ ROWSETEXT

Extiende las propiedades definidas para las API de conjunto de filas.

``` syntax
#define DBPROPSET_MSIDXS_ROWSETEXT \
    { 0xaa6ee6b0, 0xe828, 0x11d0, \
        { 0xb2, 0x3e, 0x00, 0xaa, 0x00, 0x47, 0xfc, 0x01 } }
```

El conjunto de propiedades \_ DBPROPSET MSIDXS \_ ROWSETEXT contiene las siguientes constantes de propiedad:

<dl> <dt>

<span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>MSIDXSPROP \_ ROWSETQUERYSTATUS
</dt> <dd>

Id. de propiedad 2. Estado de consulta del conjunto de filas. Las constantes STAT \_ \* indican el estado de ejecución y confiabilidad.

</dd> <dt>

<span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>CADENA DE CONFIGURACIÓN \_ REGIONAL DEL COMANDO MSIDXSPROP \_ \_
</dt> <dd>

Id. de propiedad 3. Cadena de configuración regional que representa el idioma y la configuración regional que se va a usar para este conjunto de filas.

</dd> <dt>

<span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>RESTRICCIÓN DE CONSULTAS \_ \_ MSIDXSPROP
</dt> <dd>

Id. de propiedad 4. Cadena de consulta asociada a este conjunto de filas.

</dd> <dt>

<span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>ÁRBOL DE ANÁLISIS \_ \_ MSIDXSPROP
</dt> <dd>

Id. de propiedad 5.

</dd> <dt>

<span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>MSIDXSPROP \_ MAX \_ RANK 
</dt> <dd>

Id. de propiedad 6.

</dd> <dt>

<span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>RESULTADOS DE MSIDXSPROP \_ \_ ENCONTRADOS
</dt> <dd>

Id. de propiedad 7.

</dd> <dt>

<span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>MSIDXSPROP \_ WHEREID
</dt> <dd>

Id. de propiedad 8.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>VERSIÓN DEL SERVIDOR MSIDXSPROP \_ \_ 
</dt> <dd>

Novedad de Windows 7. Id. de propiedad 9. La versión del servidor.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>MSIDXSPROP \_ SERVER \_ WINVER \_ MAJOR
</dt> <dd>

Id. de propiedad 10.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>MSIDXSPROP \_ SERVER \_ WINVER \_ MINOR
</dt> <dd>

Id. de propiedad 11.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>MSIDXSPROP \_ SERVER \_ NLSVERSION
</dt> <dd>

Id. de propiedad 12.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>MSIDXSPROP \_ SERVER \_ NLSVER \_ DEFINIDO 
</dt> <dd>

Id. de propiedad 13.

</dd> <dt>

<span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>MSIDXSPROP \_ SAME \_ SORTORDER \_ USED 
</dt> <dd>

Id. de propiedad 14.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para consultar MSIDXSPROP SERVER VERSION, es necesario emitir la consulta ficticia al \_ \_ servidor, como en el ejemplo siguiente.

`SELECT top 1 workid from servername.systemindex`

Una vez devuelto el conjunto de filas, llame a [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para las funcionalidades del conjunto de filas y, a continuación, llame a [IRowsetInfo::GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) para la nueva propiedad (MSIDXSPROP \_ SERVER \_ VERSION). La propiedad tiene un tipo de **VT \_ I4** y puede ser uno de los siguientes valores:

\#definir CI \_ VERSION \_ WDS30 0x102 // 258

\#definir CI \_ VERSION \_ WDS40 0x109 // 265

\#definir CI \_ VERSION \_ WIN70 0x700 // 1792

Una vez que se conoce el valor, el cliente puede formar una consulta que sea compatible con el servidor y emitir una consulta real.

DBPROPSET \_ MSIDXS \_ ROWSETEXT se declara en ntquery.h.

 

 
